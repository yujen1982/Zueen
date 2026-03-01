//EA交易     =>  ...\MT4\MQL4\Experts

#property  copyright "Amazing3.1"
#property version    "3.1"
#property strict

//enum ENUM_TIMEFRAMES      {PERIOD_CURRENT = 0, PERIOD_M1 = 1, PERIOD_M2 = 2, PERIOD_M3 = 3, PERIOD_M4 = 4, PERIOD_M5 = 5, PERIOD_M6 = 6, PERIOD_M10 = 10, PERIOD_M12 = 12, PERIOD_M15 = 15, PERIOD_M20 = 20, PERIOD_M30 = 30, PERIOD_H1 = 60, PERIOD_H2 = 120, PERIOD_H3 = 180, PERIOD_H4 = 240, PERIOD_H6 = 360, PERIOD_H8 = 480, PERIOD_H12 = 720, PERIOD_D1 = 1440, PERIOD_W1 = 10080, PERIOD_MN1 = 43200, };
  
 enum opentime {
      A = 1,//開單時區模式
      B = 2,//開單時間間距(秒)模式
      C = 3,//不延遲模式
          };

//------------------
extern double On_top_of_this_price_not_Buy_first_order=0  ;    //B以上不開(首)
extern double On_under_of_this_price_not_Sell_first_order=0  ;    //S以下不開(首)
extern double On_top_of_this_price_not_Buy_order=0  ;    //B以上不開(補)
extern double On_under_of_this_price_not_Sell_order=0  ;    //S以下不開(補)
extern string Limit_StartTime="00:00"  ;   //限價開始時間
extern string Limit_StopTime="24:00"  ;   //限價結束時間
extern bool CloseBuySell=true  ;    //逆勢保護開關
extern bool HomeopathyCloseAll=true  ;    //順勢保護開關
extern bool Homeopathy=false ;    //完全對鎖時掛上順勢開關
extern bool Over=false ;    //平倉後停止交易
extern int   NextTime=0  ;    //整體平倉後多少秒後新局
extern double Money=0  ;    //浮虧多少啟用第二參數
extern int   FirstStep=30  ;    //首單距離
extern int   MinDistance=60  ;    //最小距離
extern int   TwoMinDistance=60  ;    //第二最小距離
extern int   StepTrallOrders=5  ;    //掛單追蹤點數
extern int   Step=100  ;    //補單間距
extern int   TwoStep=100  ;    //第二補單間距
extern  opentime  OpenMode=3  ;   
extern  ENUM_TIMEFRAMES  TimeZone=1  ;    //開單時區
extern int   sleep=30  ;    //開單時間間距(秒)
extern double MaxLoss=100000  ;    //單邊浮虧超過多少不繼續加倉
extern double MaxLossCloseAll=50  ;    //單邊平倉限製
extern double lot=0.01  ;    //起始手數
extern double Maxlot=10  ;    //最大開單手數
extern double PlusLot=0  ;    //累加手數
extern double K_Lot=1.3  ;    //倍率
extern int   DigitsLot=2  ;    //下單量的小數位
extern double CloseAll=0.5  ;    //整體平倉金額
extern bool Profit=true  ;    //單邊平倉金額累加開關
extern double StopProfit=2  ;    //單邊平倉金額
extern double StopLoss=0  ;    //止損金額
extern int   Magic=9453  ;   
extern int   Totals=50  ;    //最大單量
extern int   MaxSpread=32  ;    //點差限製
extern int   Leverage=100  ;    //平臺杠桿限製
extern string EA_StartTime="00:00"  ;   //EA開始時間
extern string EA_StopTime="24:00"  ;   //EA結束時間

// ================== 新增ATR模组参数 ==================
extern bool UseATR = false;          // 使用ATR模组
extern int ATRPeriod = 14;           // ATR周期
extern double ATRMultiplier = 2.0;   // ATR乘数，用于动态止损
// ================== 新增最大回撤模组参数 ==================
extern bool UseMaxDrawdown = false;  // 使用最大回撤模组
extern double MaxDrawdownPercent = 20; // 最大回撤百分比（相对于峰值）
extern int DrawdownAction = 0;       // 0:只报警(不操作),1:停止加仓,2:平仓所有

 bool      總_bo_1 = true;
 bool      總_bo_2 = true;
 int       總_in_3 = 1;
 int       總_in_4 = 0;
 int       總_in_5 = 10;
 uint      總_ui_6 = Lime;
 uint      總_ui_7 = Blue;
 uint      總_ui_8 = Red;
 datetime  總_da_9 = 0;
 bool      總_bo_10 = true;
 bool      總_bo_11 = false;
 bool      總_bo_12 = false;
 string    總_st_13  =  "";
 string    總_st_14  =  "0-off  1-Candle  2-Fractals  >2-pips";
 int       總_in_15 = 3;
 int       總_in_16 = 20;
 int       總_in_17 = 25;
 int       總_in_18 = 0;
 int       總_in_19 = 15;
 int       總_in_20 = 0;
 int       總_in_21 = 346856;
 int       總_in_22 = 0;
 double    總_do_23 = 0.0;
 double    總_do_24 = 0.0;
 int       總_in_25 = 1482134400;
 string    總_st_26  =  "Exness Ltd.";
 string    總_st_27  =  "CB Financial Services Limited";
 int       總_in_28 = 1;
 int       總_in_29 = 2;
 double    總_do_30 = 10.0;
 uint      總_ui_31 = DimGray;
 string    總_st_32  =  "Spread";
 int       總_in_33 = 0;
 bool      總_bo_34 = true;
 string    總_st_35  =  "Button1";
 string    總_st_36  =  "Button2";
 string    總_st_37  =  "Button5";
 int       總_in_38 = 55295;
 int       總_in_39 = 16777215;
 int       總_in_40 = 65280;
 int       總_in_41 = 65280;
 int       總_in_42 = 65535;
 int       總_in_43 = 12632256;
 string    總_st_44  =  "Lever";
 string    總_st_45  =  "Spreads";
 int       總_in_46 = 0;
 int       總_in_47 = 25;
 int       總_in_48 = 180;
 bool      總_bo_49 = false;
 string    總_st_50  =  "Amazing3.1";
 double    總_do_51 = 0.0;
 double    總_do_52 = 0.0;
 int       總_in_53 = 0;
 int       總_in_54 = 0;
 int       總_in_55 = 0;
 string    總_st_56  =  "000,000,000";
 string    總_st_57  =  "000,000,255";
 int       總_in_58 = 40;
 int       總_in_59 = 0;
 int       總_in_60 = 0;
 int       總_in_61 = 0;
 datetime  總_da_62 = 0;
 datetime  總_da_63 = 0;
 datetime  總_da_64 = 0;
 datetime  總_da_65 = 0;
 datetime  總_da_66 = 0;
 datetime  總_da_67 = 0;
 datetime  總_da_68 = 0;
 int       總_in_69 = 0;

// ================== 新增全局变量 ==================
double    總_atrValue = 0.0;          // 当前ATR值
double    總_peakEquity = 0.0;        // 历史峰值净值
bool      總_drawdownTriggered = false; // 是否已触发回撤警告/动作
int       總_drawdownActionDone = 0;     // 已执行的动作类型
bool      總_bo_drawdownStop = false;    // 回撤停止加仓标志

 int init ()
 {
 int         子_in_1;
 bool        子_bo_2;
 string      子_st_3;
 int         子_in_4;

//----------------------------


  總_st_50 = WindowExpertName() ;
 
 子_in_1 = 0 ;
 子_bo_2 = false ;
 子_in_4 = 0 ;
 總_in_19 = lizong_8(總_in_19) ;
 if ( ( Digits() == 5 || Digits() == 3 ) )
  {
  總_in_22 = 30 ;
  }
 Comment(""); 
 總_in_20=MathMax(MarketInfo(Symbol(),33),MarketInfo(Symbol(),14)) + 1;
 if ( Step <  總_in_20 )
  {
  Step = 總_in_20 ;
  }
 if ( FirstStep <  總_in_20 )
  {
  FirstStep = 總_in_20 ;
  }
 if ( MinDistance <  總_in_20 )
  {
  MinDistance = 總_in_20 ;
  }
 if ( 總_bo_34 )
  {
  ObjectCreate(0,總_st_35,OBJ_BUTTON,0,0,0.0); 
  ObjectSetInteger(0,總_st_35,OBJPROP_CORNER,2); 
  ObjectSetInteger(0,總_st_35,OBJPROP_COLOR,16777215); 
  ObjectSetInteger(0,總_st_35,OBJPROP_BGCOLOR,6908265); 
  ObjectSetInteger(0,總_st_35,OBJPROP_BORDER_COLOR,16777215); 
  ObjectSetInteger(0,總_st_35,OBJPROP_XDISTANCE,0); 
  ObjectSetInteger(0,總_st_35,OBJPROP_YDISTANCE,30); 
  ObjectSetInteger(0,總_st_35,OBJPROP_XSIZE,55); 
  ObjectSetInteger(0,總_st_35,OBJPROP_YSIZE,30); 
  ObjectSetString(0,總_st_35,OBJPROP_FONT,"黑體"); 
  ObjectSetString(0,總_st_35,OBJPROP_TEXT,"C buy"); 
  ObjectSetInteger(0,總_st_35,OBJPROP_FONTSIZE,15); 
  ObjectSetInteger(0,總_st_35,OBJPROP_SELECTABLE,1); 
  ObjectSetInteger(0,總_st_35,OBJPROP_SELECTED,0); 
  ObjectCreate(0,總_st_36,OBJ_BUTTON,0,0,0.0); 
  ObjectSetInteger(0,總_st_36,OBJPROP_CORNER,2); 
  ObjectSetInteger(0,總_st_36,OBJPROP_COLOR,16777215); 
  ObjectSetInteger(0,總_st_36,OBJPROP_BGCOLOR,6908265); 
  ObjectSetInteger(0,總_st_36,OBJPROP_BORDER_COLOR,16777215); 
  ObjectSetInteger(0,總_st_36,OBJPROP_XDISTANCE,60); 
  ObjectSetInteger(0,總_st_36,OBJPROP_YDISTANCE,30); 
  ObjectSetInteger(0,總_st_36,OBJPROP_XSIZE,55); 
  ObjectSetInteger(0,總_st_36,OBJPROP_YSIZE,30); 
  ObjectSetString(0,總_st_36,OBJPROP_FONT,"黑體"); 
  ObjectSetString(0,總_st_36,OBJPROP_TEXT,"C sel"); 
  ObjectSetInteger(0,總_st_36,OBJPROP_FONTSIZE,15); 
  ObjectSetInteger(0,總_st_36,OBJPROP_SELECTABLE,1); 
  ObjectSetInteger(0,總_st_36,OBJPROP_SELECTED,0); 
  ObjectCreate(0,總_st_37,OBJ_BUTTON,0,0,0.0); 
  ObjectSetInteger(0,總_st_37,OBJPROP_CORNER,2); 
  ObjectSetInteger(0,總_st_37,OBJPROP_COLOR,16777215); 
  ObjectSetInteger(0,總_st_37,OBJPROP_BGCOLOR,6908265); 
  ObjectSetInteger(0,總_st_37,OBJPROP_BORDER_COLOR,16777215); 
  ObjectSetInteger(0,總_st_37,OBJPROP_XDISTANCE,30); 
  ObjectSetInteger(0,總_st_37,OBJPROP_YDISTANCE,70); 
  ObjectSetInteger(0,總_st_37,OBJPROP_XSIZE,55); 
  ObjectSetInteger(0,總_st_37,OBJPROP_YSIZE,30); 
  ObjectSetString(0,總_st_37,OBJPROP_FONT,"黑體"); 
  ObjectSetString(0,總_st_37,OBJPROP_TEXT,"Close"); 
  ObjectSetInteger(0,總_st_37,OBJPROP_FONTSIZE,15); 
  ObjectSetInteger(0,總_st_37,OBJPROP_SELECTABLE,1); 
  ObjectSetInteger(0,總_st_37,OBJPROP_SELECTED,0); 
  }
 子_in_1 = 總_in_5 + 總_in_5 / 2;
 ObjectCreate("Balance",OBJ_LABEL,0,0,0.0,0,0.0,0,0.0); 
 ObjectSet("Balance",OBJPROP_CORNER,1.0); 
 ObjectSet("Balance",OBJPROP_XDISTANCE,5.0); 
 ObjectSet("Balance",OBJPROP_YDISTANCE,子_in_1); 
 子_in_1 = 子_in_1 + 總_in_5 * 2;
 ObjectCreate("Equity",OBJ_LABEL,0,0,0.0,0,0.0,0,0.0); 
 ObjectSet("Equity",OBJPROP_CORNER,1.0); 
 ObjectSet("Equity",OBJPROP_XDISTANCE,5.0); 
 ObjectSet("Equity",OBJPROP_YDISTANCE,子_in_1); 
 子_in_1 = 子_in_1 + 總_in_5 * 2;
 ObjectCreate("FreeMargin",OBJ_LABEL,0,0,0.0,0,0.0,0,0.0); 
 ObjectSet("FreeMargin",OBJPROP_CORNER,1.0); 
 ObjectSet("FreeMargin",OBJPROP_XDISTANCE,5.0); 
 ObjectSet("FreeMargin",OBJPROP_YDISTANCE,子_in_1); 
 子_in_1 = 子_in_1 + 總_in_5 * 2;
 ObjectCreate("ProfitB",OBJ_LABEL,0,0,0.0,0,0.0,0,0.0); 
 ObjectSet("ProfitB",OBJPROP_CORNER,1.0); 
 ObjectSet("ProfitB",OBJPROP_XDISTANCE,5.0); 
 ObjectSet("ProfitB",OBJPROP_YDISTANCE,子_in_1); 
 子_in_1 = 子_in_1 + 總_in_5 * 2;
 ObjectCreate("ProfitS",OBJ_LABEL,0,0,0.0,0,0.0,0,0.0); 
 ObjectSet("ProfitS",OBJPROP_CORNER,1.0); 
 ObjectSet("ProfitS",OBJPROP_XDISTANCE,5.0); 
 ObjectSet("ProfitS",OBJPROP_YDISTANCE,子_in_1); 
 子_in_1 = 子_in_1 + 總_in_5 * 2;
 ObjectCreate("Profit",OBJ_LABEL,0,0,0.0,0,0.0,0,0.0); 
 ObjectSet("Profit",OBJPROP_CORNER,1.0); 
 ObjectSet("Profit",OBJPROP_XDISTANCE,5.0); 
 ObjectSet("Profit",OBJPROP_YDISTANCE,子_in_1); 
 子_in_1 = 子_in_1 + 總_in_5 * 3;
 子_bo_2 = false ;
 子_st_3 = "Paramfalse" ;
 MaxLossCloseAll = -(MaxLossCloseAll);
 MaxLoss = -(MaxLoss);
 StopLoss = -(StopLoss);
 Money = -(Money);

 if ( 總_st_50  !=  WindowExpertName() )
  {
  Comment(""); 
  總_bo_1 = false ;
  總_bo_2 = false ;
  ObjectsDeleteAll(-1,-1); 
  if ( ObjectFind(總_st_32) <  0 )
   {
   ObjectCreate(總_st_32,OBJ_LABEL,0,0,0.0,0,0.0,0,0.0); 
   ObjectSet(總_st_32,OBJPROP_CORNER,1.0); 
   ObjectSet(總_st_32,OBJPROP_YDISTANCE,260.0); 
   ObjectSet(總_st_32,OBJPROP_XDISTANCE,10.0); 
   ObjectSetText(總_st_32,"Spread: " + DoubleToString((Ask - Bid) / 總_do_30,1) + " pips",13,"Arial",總_ui_31); 
   }
  ObjectSetText(總_st_32,"Spread: " + DoubleToString((Ask - Bid) / 總_do_30,1) + " pips",0,NULL,0xFFFFFFFF); 
  WindowRedraw(); 
  WindowRedraw(); 
  }
 PlaySound("Starting.wav"); 
 StringReplace(EA_StartTime," ",""); 
 StringReplace(EA_StopTime," ",""); 
 StringTrimLeft(EA_StartTime); 
 StringTrimLeft(EA_StopTime); 
 StringTrimRight(EA_StartTime); 
 StringTrimRight(EA_StopTime); 
 if ( EA_StopTime == "24:00" )
  {
  EA_StopTime = "23:59:59" ;
  }
 StringReplace(Limit_StartTime," ",""); 
 StringReplace(Limit_StopTime," ",""); 
 StringTrimLeft(Limit_StartTime); 
 StringTrimLeft(Limit_StopTime); 
 StringTrimRight(Limit_StartTime); 
 StringTrimRight(Limit_StopTime); 
 if ( Limit_StopTime == "24:00" )
  {
  Limit_StopTime = "23:59:59" ;
  }

 // ================== 新增变量初始化 ==================
 總_atrValue = 0.0;
 總_peakEquity = AccountEquity();
 總_drawdownTriggered = false;
 總_drawdownActionDone = 0;
 總_bo_drawdownStop = false;

 return(0); 
 }
//init
//---------------------  ----------------------------------------

 int start ()
 {
 bool        子_bo_1;
 double      子_do_2;
 double      子_do_3;
 double      子_do_4;
 double      子_do_5;
 double      子_do_6;
 double      子_do_7;
 int         子_in_8;
 int         子_in_9;
 int         子_in_10;
 int         子_in_11;
 int         子_in_12;
 int         子_in_13;
 int         子_in_14;
 double      子_do_15;
 double      子_do_16;
 double      子_do_17;
 double      子_do_18;
 double      子_do_19;
 double      子_do_20;
 double      子_do_21;
 double      子_do_22;
 double      子_do_23;
 double      子_do_24;
 double      子_do_25;
 double      子_do_26;
 int         子_in_27;
 double      子_do_28;
 string      子_st_29;
 double      子_do_30;
 string      子_st_31;
 double      子_do_32;
 double      子_do_33;
 bool        子_bo_34;
 double      子_do_35;
 double      子_do_36;
 double      子_do_37;
 double      子_do_38;
 double      子_do_39;

//----------------------------
 datetime   臨_da_1;
 bool       臨_bo_2;
 string     臨_st_3;
 string     臨_st_4;
 string     臨_st_5;
 string     臨_st_6;
 datetime   臨_da_7;
 bool       臨_bo_8;
 string     臨_st_9;
 string     臨_st_10;
 string     臨_st_11;
 string     臨_st_12;
 datetime   臨_da_13;
 bool       臨_bo_14;
 string     臨_st_15;
 string     臨_st_16;
 string     臨_st_17;
 string     臨_st_18;
 int        臨_in_19;
 double     臨_do_20;
 int        臨_in_21;
 double     臨_do_22;
 int        臨_in_23;
 string     臨_st_24;
 string     臨_st_25;
 int        臨_in_26;
 double     臨_do_27;
 int        臨_in_28;
 double     臨_do_29;
 string     臨_st_30;
 string     臨_st_31;
 int        臨_in_32;
 double     臨_do_33;
 int        臨_in_34;
 double     臨_do_35;
 int        臨_in_36;
 string     臨_st_37;
 string     臨_st_38;
 int        臨_in_39;
 double     臨_do_40;
 int        臨_in_41;
 double     臨_do_42;
 string     臨_st_43;
 int        臨_in_44;
 int        臨_in_45;
 string     臨_st_46;
 int        臨_in_47;
 int        臨_in_48;
 string     臨_st_49;
 int        臨_in_50;
 int        臨_in_51;
 string     臨_st_52;
 int        臨_in_53;
 int        臨_in_54;
 string     臨_st_55;
 string     臨_st_56;
 int        臨_in_57;
 double     臨_do_58;
 int        臨_in_59;
 double     臨_do_60;
 int        臨_in_61;
 string     臨_st_62;
 string     臨_st_63;
 int        臨_in_64;
 double     臨_do_65;
 int        臨_in_66;
 double     臨_do_67;
 string     臨_st_68;
 string     臨_st_69;
 int        臨_in_70;
 double     臨_do_71;
 int        臨_in_72;
 double     臨_do_73;
 int        臨_in_74;
 string     臨_st_75;
 string     臨_st_76;
 int        臨_in_77;
 double     臨_do_78;
 int        臨_in_79;
 double     臨_do_80;
 string     臨_st_81;
 string     臨_st_82;
 int        臨_in_83;
 double     臨_do_84;
 int        臨_in_85;
 double     臨_do_86;
 int        臨_in_87;
 string     臨_st_88;
 string     臨_st_89;
 int        臨_in_90;
 double     臨_do_91;
 int        臨_in_92;
 double     臨_do_93;
 string     臨_st_94;
 string     臨_st_95;
 int        臨_in_96;
 double     臨_do_97;
 int        臨_in_98;
 double     臨_do_99;
 int        臨_in_100;
 string     臨_st_101;
 string     臨_st_102;
 int        臨_in_103;
 double     臨_do_104;
 int        臨_in_105;
 double     臨_do_106;
 int        臨_in_107;
 int        臨_in_108;
 int        臨_in_109;
 double     臨_do_110;
 double     臨_do_111;
 int        臨_in_112;
 int        臨_in_113;
 int        臨_in_114;
 int        臨_in_115;
 double     臨_do_116;
 double     臨_do_117;
 int        臨_in_118;
 datetime   臨_da_119;
 bool       臨_bo_120;
 datetime   臨_da_121;
 bool       臨_bo_122;
 datetime   臨_da_123;
 bool       臨_bo_124;
 datetime   臨_da_125;
 bool       臨_bo_126;
 datetime   臨_da_127;
 bool       臨_bo_128;
 datetime   臨_da_129;
 bool       臨_bo_130;
 int        臨_in_131;
 int        臨_in_132;
 int        臨_in_133;
 int        臨_in_134;
 int        臨_in_135;
 datetime   臨_da_136;
 bool       臨_bo_137;
 datetime   臨_da_138;
 bool       臨_bo_139;
 datetime   臨_da_140;
 bool       臨_bo_141;
 datetime   臨_da_142;
 bool       臨_bo_143;
 datetime   臨_da_144;
 bool       臨_bo_145;
 datetime   臨_da_146;
 bool       臨_bo_147;
 int        臨_in_148;
 int        臨_in_149;
 int        臨_in_150;
 int        臨_in_151;
 int        臨_in_152;
 int        臨_in_153;
 int        臨_in_154;
 int        臨_in_155;


 switch(AccountNumber())
  {
  case 5320061 :
   子_bo_1 = true ;
      break;
  case 200007738 :
   子_bo_1 = true ;
      break;
  case 10048166 :
   子_bo_1 = false ;
      break;
  case 7061521 :
   子_bo_1 = false ;
      break;
  case 12456 :
   子_bo_1 = false ;
      break;
  default :
   子_bo_1 = false ;
  }
 if ( IsDemo() )
  {
  子_bo_1 = true ;
  }
 if ( IsTesting() )
  {
  子_bo_1 = true ;
  }
/* if (1>2 && !(子_bo_1) )
  {
  Alert("非法帳戶" + string(AccountNumber()) + "\n" + "請與 QQ 3372807677 聯絡!"); 
  總_bo_1 = false ;
  總_bo_2 = false ;
  ObjectsDeleteAll(-1,-1); 
  ExpertRemove(); 
  WindowRedraw(); 
  return(0); 
  }
  */
 臨_da_1 = 0;
 if ( IsTesting() )
  {
  臨_da_1 = TimeCurrent();
  }
 else
  {
  臨_da_1 = TimeLocal();
  }
 總_da_65 = StringToTime(StringConcatenate(TimeYear(臨_da_1),".",TimeMonth(臨_da_1),".",TimeDay(臨_da_1)," ",Limit_StartTime)) ;
 總_da_66 = StringToTime(StringConcatenate(TimeYear(臨_da_1),".",TimeMonth(臨_da_1),".",TimeDay(臨_da_1)," ",Limit_StopTime)) ;
 if ( 總_da_65 <  總_da_66 && ( 臨_da_1 < 總_da_63 || 臨_da_1 > 總_da_66 ) )
  {
  ObjectDelete("HLINE_LONG"); 
  ObjectDelete("HLINE_SHORT"); 
  ObjectDelete("HLINE_LONGII"); 
  ObjectDelete("HLINE_SHORTII"); 
  臨_bo_2 = false;
  }
 else
  {
  if ( 總_da_65 > 總_da_66 && 臨_da_1 <  總_da_65 && 臨_da_1 > 總_da_66 )
   {
   ObjectDelete("HLINE_LONG"); 
   ObjectDelete("HLINE_SHORT"); 
   ObjectDelete("HLINE_LONGII"); 
   ObjectDelete("HLINE_SHORTII"); 
   臨_bo_2 = false;
   }
  else
   {
   臨_bo_2 = true;
  }}
 if ( 臨_bo_2 )
  {
  if ( On_top_of_this_price_not_Buy_first_order!=0.0 )
   {
   ObjectCreate(0,"HLINE_LONG",OBJ_HLINE,0,0,On_top_of_this_price_not_Buy_first_order); 
   ObjectSet("HLINE_LONG",OBJPROP_STYLE,0.0); 
   ObjectSet("HLINE_LONG",OBJPROP_COLOR,10025880.0); 
   }
  if ( On_under_of_this_price_not_Sell_first_order!=0.0 )
   {
   ObjectCreate(0,"HLINE_SHORT",OBJ_HLINE,0,0,On_under_of_this_price_not_Sell_first_order); 
   ObjectSet("HLINE_SHORT",OBJPROP_STYLE,0.0); 
   ObjectSet("HLINE_SHORT",OBJPROP_COLOR,16711935.0); 
   }
  if ( On_top_of_this_price_not_Buy_order!=0.0 )
   {
   ObjectCreate(0,"HLINE_LONGII",OBJ_HLINE,0,0,On_top_of_this_price_not_Buy_order); 
   ObjectSet("HLINE_LONGII",OBJPROP_STYLE,2.0); 
   ObjectSet("HLINE_LONGII",OBJPROP_COLOR,10025880.0); 
   }
  if ( On_under_of_this_price_not_Sell_order!=0.0 )
   {
   ObjectCreate(0,"HLINE_SHORTII",OBJ_HLINE,0,0,On_under_of_this_price_not_Sell_order); 
   ObjectSet("HLINE_SHORTII",OBJPROP_STYLE,2.0); 
   ObjectSet("HLINE_SHORTII",OBJPROP_COLOR,16711935.0); 
  }}
 子_do_2 = 0.0 ;
 子_do_3 = 0.0 ;
 子_do_4 = 0.0 ;
 子_do_5 = 0.0 ;
 子_do_6 = 0.0 ;
 子_do_7 = 0.0 ;
 子_in_8 = 0 ;
 子_in_9 = 0 ;
 子_in_10 = 0 ;
 子_in_11 = 0 ;
 子_in_12 = 0 ;
 子_in_13 = 0 ;
 子_in_14 = 0 ;
 子_do_15 = 0.0 ;
 子_do_16 = 0.0 ;
 子_do_17 = 0.0 ;
 子_do_18 = 0.0 ;
 子_do_19 = 0.0 ;
 子_do_20 = 0.0 ;
 子_do_21 = 0.0 ;
 子_do_22 = 0.0 ;
 子_do_23 = 0.0 ;
 子_do_24 = 0.0 ;
 子_do_25 = 0.0 ;
 子_do_26 = 0.0 ;
 子_in_27 = 0 ;
 子_do_28 = 0.0 ;
 子_do_30 = 0.0 ;
 子_do_32 = 0.0 ;
 子_do_33 = 0.0 ;
 子_bo_34 = false ;
 for (子_in_27 = 0 ; 子_in_27 < OrdersTotal() ; 子_in_27 = 子_in_27 + 1)
  {
  if ( !(OrderSelect(子_in_27,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || Magic != OrderMagicNumber() )   continue;
  子_in_12 = OrderType() ;
  子_do_7 = OrderLots() ;
  子_do_2 = NormalizeDouble(OrderOpenPrice(),Digits()) ;
  if ( 子_in_12 == 4 )
   {
   子_in_10 = 子_in_10 + 1;
   if ( ( 子_do_15<子_do_2 || 子_do_15==0.0 ) )
    {
    子_do_15 = 子_do_2 ;
    }
   子_in_13 = OrderTicket() ;
   子_do_19 = 子_do_2 ;
   }
  if ( 子_in_12 == 5 )
   {
   子_in_11 = 子_in_11 + 1;
   if ( ( 子_do_18>子_do_2 || 子_do_18==0.0 ) )
    {
    子_do_18 = 子_do_2 ;
    }
   子_in_14 = OrderTicket() ;
   子_do_20 = 子_do_2 ;
   }
  if ( 子_in_12 == 0 )
   {
   子_in_8 = 子_in_8 + 1;
   子_do_5 = 子_do_5 + 子_do_7 ;
   子_do_22 = 子_do_2 * 子_do_7 + 子_do_22 ;
   if ( ( 子_do_15<子_do_2 || 子_do_15==0.0 ) )
    {
    子_do_15 = 子_do_2 ;
    }
   if ( ( 子_do_16>子_do_2 || 子_do_16==0.0 ) )
    {
    子_do_16 = 子_do_2 ;
    }
   子_do_4 = OrderProfit() + OrderSwap() + OrderCommission() + 子_do_4 ;
   }
  if ( 子_in_12 != 1 )   continue;
  子_in_9 = 子_in_9 + 1;
  子_do_6 = 子_do_6 + 子_do_7 ;
  子_do_21 = 子_do_2 * 子_do_7 + 子_do_21 ;
  if ( ( 子_do_18>子_do_2 || 子_do_18==0.0 ) )
   {
   子_do_18 = 子_do_2 ;
   }
  if ( ( 子_do_17<子_do_2 || 子_do_17==0.0 ) )
   {
   子_do_17 = 子_do_2 ;
   }
  子_do_3 = OrderProfit() + OrderSwap() + OrderCommission() + 子_do_3 ;
  }

 // ================== 新增ATR止损模组（增加ATR值为0检查） ==================
 if (UseATR)
 {
     總_atrValue = iATR(Symbol(), 0, ATRPeriod, 0);
     if (總_atrValue == 0) // 数据不足，跳过本次
     {
         Print("ATR value is 0, skipping ATR stop loss this tick.");
     }
     else
     {
         double atrPoints = 總_atrValue / Point();
         // 遍历所有持仓订单，进行ATR止损
         for (int i = OrdersTotal()-1; i >= 0; i--)
         {
             if (OrderSelect(i, SELECT_BY_POS, MODE_TRADES) && OrderSymbol()==Symbol() && OrderMagicNumber()==Magic)
             {
                 int type = OrderType();
                 if (type == 0 || type == 1)
                 {
                     double lossPoints = 0;
                     if (type == 0) // 多单
                         lossPoints = (OrderOpenPrice() - Bid) / Point;
                     else // 空单
                         lossPoints = (Ask - OrderOpenPrice()) / Point;
                     
                     if (lossPoints >= atrPoints * ATRMultiplier)
                     {
                         // 平仓该订单
                         double closePrice = (type==0) ? Bid : Ask;
                         OrderClose(OrderTicket(), OrderLots(), closePrice, 5, clrNONE);
                     }
                 }
             }
         }
     }
 }

 if ( 子_do_4>0.0 )
  {
  ObjectSetInteger(0,總_st_35,OBJPROP_BGCOLOR,17919); 
  }
 else
  {
  ObjectSetInteger(0,總_st_35,OBJPROP_BGCOLOR,6908265); 
  }
 if ( 子_do_3>0.0 )
  {
  ObjectSetInteger(0,總_st_36,OBJPROP_BGCOLOR,17919); 
  }
 else
  {
  ObjectSetInteger(0,總_st_36,OBJPROP_BGCOLOR,6908265); 
  }
 if ( 子_do_4 + 子_do_3>0.0 )
  {
  ObjectSetInteger(0,總_st_37,OBJPROP_BGCOLOR,17919); 
  }
 else
  {
  ObjectSetInteger(0,總_st_37,OBJPROP_BGCOLOR,6908265); 
  }
 if ( 子_do_5>0.0 && 子_do_6 / 子_do_5>3.0 && 子_do_6 - 子_do_5>0.2 )
  {
  總_bo_11 = true ;
  }
 else
  {
  總_bo_11 = false ;
  }
 if ( 子_do_6>0.0 && 子_do_5 / 子_do_6>3.0 && 子_do_5 - 子_do_6>0.2 )
  {
  總_bo_12 = true ;
  }
 else
  {
  總_bo_12 = false ;
  }
 子_do_35 = 0.0 ;
 子_do_36 = 0.0 ;
 子_do_37 = 0.0 ;
 子_do_38 = 0.0 ;
 子_do_35 = iHigh(Symbol(),總_in_3,0) - iLow(Symbol(),總_in_3,5) ;
 子_do_37 = iLow(Symbol(),總_in_3,0) - iHigh(Symbol(),總_in_3,5) ;
 子_do_36 = int(子_do_35 / Point()) ;
 子_do_38 = MathAbs(子_do_37 / Point()) ;
 if ( ( AccountLeverage() < Leverage || IsTradeAllowed() == false || IsExpertEnabled() == false || IsStopped() || 子_in_8 + 子_in_9 >= Totals || MarketInfo(Symbol(),13)>MaxSpread || ( 總_in_4 != 0 && 子_do_36>=總_in_4 ) || (總_in_4 != 0 && 子_do_38>=總_in_4) ) )
  {
  總_bo_1 = false ;
  總_bo_2 = false ;
  臨_st_3 = "Arial";
  臨_st_4 = "This EA has stop work ! ";
  if ( ObjectFind("Stop") == -1 )
   {
   ObjectCreate("Stop",OBJ_LABEL,0,0,0.0,0,0.0,0,0.0); 
   ObjectSet("Stop",OBJPROP_CORNER,總_in_46); 
   ObjectSet("Stop",OBJPROP_XDISTANCE,總_in_47); 
   ObjectSet("Stop",OBJPROP_YDISTANCE,總_in_48 + 30); 
   }
  ObjectSetText("Stop",臨_st_4,總_in_5,臨_st_3,總_ui_31); 
  }
 else
  {
  總_bo_1 = true ;
  總_bo_2 = true ;
  臨_st_5 = "Arial";
  臨_st_6 = "";
  if ( ObjectFind("Stop") == -1 )
   {
   ObjectCreate("Stop",OBJ_LABEL,0,0,0.0,0,0.0,0,0.0); 
   ObjectSet("Stop",OBJPROP_CORNER,總_in_46); 
   ObjectSet("Stop",OBJPROP_XDISTANCE,總_in_47); 
   ObjectSet("Stop",OBJPROP_YDISTANCE,總_in_48 + 30); 
   }
  ObjectSetText("Stop",臨_st_6,總_in_5,臨_st_5,總_ui_31); 
  }
 臨_da_7 = 0;
 if ( IsTesting() )
  {
  臨_da_7 = TimeCurrent();
  }
 else
  {
  臨_da_7 = TimeLocal();
  }
 總_da_63 = StringToTime(StringConcatenate(TimeYear(臨_da_7),".",TimeMonth(臨_da_7),".",TimeDay(臨_da_7)," ",EA_StartTime)) ;
 總_da_64 = StringToTime(StringConcatenate(TimeYear(臨_da_7),".",TimeMonth(臨_da_7),".",TimeDay(臨_da_7)," ",EA_StopTime)) ;
 if ( 總_da_63 <  總_da_64 && ( 臨_da_7 < 總_da_63 || 臨_da_7 > 總_da_64 ) )
  {
  臨_bo_8 = false;
  }
 else
  {
  if ( 總_da_63 > 總_da_64 && 臨_da_7 <  總_da_63 && 臨_da_7 > 總_da_64 )
   {
   臨_bo_8 = false;
   }
  else
   {
   臨_bo_8 = true;
  }}
 if ( !(臨_bo_8) )
  {
  臨_st_9 = "Arial";
  臨_st_10 = "Time out,This EA has stop open order";
  if ( ObjectFind("Stop") == -1 )
   {
   ObjectCreate("Stop",OBJ_LABEL,0,0,0.0,0,0.0,0,0.0); 
   ObjectSet("Stop",OBJPROP_CORNER,總_in_46); 
   ObjectSet("Stop",OBJPROP_XDISTANCE,總_in_47); 
   ObjectSet("Stop",OBJPROP_YDISTANCE,總_in_48 + 30); 
   }
  ObjectSetText("Stop",臨_st_10,總_in_5,臨_st_9,總_ui_31); 
  }
 if ( 總_st_50  !=  WindowExpertName() )
  {
  總_bo_1 = false ;
  總_bo_2 = false ;
  臨_st_11 = "Arial";
  臨_st_12 = "This EA has stop work ! ";
  if ( ObjectFind("Stop") == -1 )
   {
   ObjectCreate("Stop",OBJ_LABEL,0,0,0.0,0,0.0,0,0.0); 
   ObjectSet("Stop",OBJPROP_CORNER,總_in_46); 
   ObjectSet("Stop",OBJPROP_XDISTANCE,總_in_47); 
   ObjectSet("Stop",OBJPROP_YDISTANCE,總_in_48 + 30); 
   }
  ObjectSetText("Stop",臨_st_12,總_in_5,臨_st_11,總_ui_31); 
  }
 if ( TimeCurrent() <  總_da_9 )
  {
  臨_da_13 = 0;
  if ( IsTesting() )
   {
   臨_da_13 = TimeCurrent();
   }
  else
   {
   臨_da_13 = TimeLocal();
   }
  總_da_63 = StringToTime(StringConcatenate(TimeYear(臨_da_13),".",TimeMonth(臨_da_13),".",TimeDay(臨_da_13)," ",EA_StartTime)) ;
  總_da_64 = StringToTime(StringConcatenate(TimeYear(臨_da_13),".",TimeMonth(臨_da_13),".",TimeDay(臨_da_13)," ",EA_StopTime)) ;
  if ( 總_da_63 <  總_da_64 && ( 臨_da_13 < 總_da_63 || 臨_da_13 > 總_da_64 ) )
   {
   臨_bo_14 = false;
   }
  else
   {
   if ( 總_da_63 > 總_da_64 && 臨_da_13 <  總_da_63 && 臨_da_13 > 總_da_64 )
    {
    臨_bo_14 = false;
    }
   else
    {
    臨_bo_14 = true;
   }}
  if ( 臨_bo_14 )
   {
   總_bo_1 = false ;
   總_bo_2 = false ;
   臨_st_15 = "Arial";
   臨_st_16 = "This EA has stop work " + string(NextTime) + "second! ";
   if ( ObjectFind("Stop") == -1 )
    {
    ObjectCreate("Stop",OBJ_LABEL,0,0,0.0,0,0.0,0,0.0); 
    ObjectSet("Stop",OBJPROP_CORNER,總_in_46); 
    ObjectSet("Stop",OBJPROP_XDISTANCE,總_in_47); 
    ObjectSet("Stop",OBJPROP_YDISTANCE,總_in_48 + 30); 
    }
   ObjectSetText("Stop",臨_st_16,總_in_5,臨_st_15,總_ui_31); 
  }}
 if ( Over == 1 && 子_in_8 == 0 )
  {
  總_bo_1 = false ;
  }
 if ( Over == 1 && 子_in_9 == 0 )
  {
  總_bo_2 = false ;
  }
 ObjectDelete("SLb"); 
 ObjectDelete("SLs"); 
 if ( 子_in_8 > 0 )
  {
  子_do_23 = NormalizeDouble(子_do_22 / 子_do_5,Digits()) ;
  ObjectCreate("SLb",OBJ_ARROW,0,Time[0],子_do_23,0,0.0,0,0.0); 
  ObjectSet("SLb",OBJPROP_ARROWCODE,6.0); 
  ObjectSet("SLb",OBJPROP_COLOR,總_ui_7); 
  }
 if ( 子_in_9 > 0 )
  {
  子_do_24 = NormalizeDouble(子_do_21 / 子_do_6,Digits()) ;
  ObjectCreate("SLs",OBJ_ARROW,0,Time[0],子_do_24,0,0.0,0,0.0); 
  ObjectSet("SLs",OBJPROP_ARROWCODE,6.0); 
  ObjectSet("SLs",OBJPROP_COLOR,總_ui_8); 
  }
 ObjectSetText("Char.op",CharToString(74),總_in_5 + 2,"Wingdings",Red); 
 子_do_39 = 子_do_4 + 子_do_3 ;

 // ================== 新增最大回撤模组 ==================
 if (UseMaxDrawdown)
 {
     double currentEquity = AccountEquity();
     if (currentEquity > 總_peakEquity)
         總_peakEquity = currentEquity;
     
     double drawdownPercent = 0.0;
     if (總_peakEquity > 0)
         drawdownPercent = (總_peakEquity - currentEquity) / 總_peakEquity * 100.0;
     
     if (drawdownPercent >= MaxDrawdownPercent && !總_drawdownTriggered)
     {
         總_drawdownTriggered = true;
         總_drawdownActionDone = DrawdownAction;
         
         if (DrawdownAction == 1)
         {
             總_bo_drawdownStop = true; // 停止加仓
             Print("最大回撤达到 ", DoubleToString(drawdownPercent,2), "%，已停止加仓");
         }
         else if (DrawdownAction == 2)
         {
             // 平仓所有订单
             lizong_7(0);
             總_bo_drawdownStop = true; // 平仓后也停止加仓
             Print("最大回撤达到 ", DoubleToString(drawdownPercent,2), "%，已平仓所有订单并停止加仓");
         }
         else // DrawdownAction == 0 只报警
         {
             Print("警告：最大回撤达到 ", DoubleToString(drawdownPercent,2), "%");
         }
     }
     else if (drawdownPercent < MaxDrawdownPercent)
     {
         總_drawdownTriggered = false; // 如果回撤恢复，重置标志（但动作不会重复执行，因为已經記錄done）
         // 对于停止加仓的情况，我们可能不希望自动恢复，所以不重置 總_bo_drawdownStop
     }
 }

 if ( Over == 1 && 子_do_39>=CloseAll )
  {
  總_bo_1 = false ;
  總_bo_2 = false ;
  臨_st_17 = "Ticket";
  臨_st_18 = "sell";
  臨_in_19 = 0;
  臨_do_20 = 0.0;
  for (臨_in_21 = OrdersTotal() - 1 ; 臨_in_21 >= 0 ; 臨_in_21 = 臨_in_21 - 1)
   {
   if ( !(OrderSelect(臨_in_21,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
   
   if ( 臨_st_18 == "buy" && OrderType() == 0 && OrderTicket() > 臨_in_19 )
    {
    OrderOpenTime(); 
    OrderOpenPrice(); 
    臨_do_20 = OrderLots();
    臨_in_19 = OrderTicket();
    }
   if ( 臨_st_18 != "sell" || OrderType() != 1 || OrderTicket() <= 臨_in_19 )   continue;
   OrderOpenTime(); 
   OrderOpenPrice(); 
   臨_do_20 = OrderLots();
   臨_in_19 = OrderTicket();
   }
  if ( 臨_st_17 == "Ticket" )
   {
   臨_do_22 = 臨_in_19;
   }
  else
   {
   if ( 臨_st_17 == "Lots" )
    {
    臨_do_22 = 臨_do_20;
    }
   else
    {
    臨_do_22 = 0.0;
   }}
  臨_in_23 = 臨_do_22;
  臨_st_24 = "Ticket";
  臨_st_25 = "buy";
  臨_in_26 = 0;
  臨_do_27 = 0.0;
  for (臨_in_28 = OrdersTotal() - 1 ; 臨_in_28 >= 0 ; 臨_in_28 = 臨_in_28 - 1)
   {
   if ( !(OrderSelect(臨_in_28,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
   
   if ( 臨_st_25 == "buy" && OrderType() == 0 && OrderTicket() > 臨_in_26 )
    {
    OrderOpenTime(); 
    OrderOpenPrice(); 
    臨_do_27 = OrderLots();
    臨_in_26 = OrderTicket();
    }
   if ( 臨_st_25 != "sell" || OrderType() != 1 || OrderTicket() <= 臨_in_26 )   continue;
   OrderOpenTime(); 
   OrderOpenPrice(); 
   臨_do_27 = OrderLots();
   臨_in_26 = OrderTicket();
   }
  if ( 臨_st_24 == "Ticket" )
   {
   臨_do_29 = 臨_in_26;
   }
  else
   {
   if ( 臨_st_24 == "Lots" )
    {
    臨_do_29 = 臨_do_27;
    }
   else
    {
    臨_do_29 = 0.0;
   }}
   if(OrderCloseBy(臨_do_29,臨_in_23,0xFFFFFFFF)){
  do
   {
   臨_st_30 = "Ticket";
   臨_st_31 = "sell";
   臨_in_32 = 0;
   臨_do_33 = 0.0;
   for (臨_in_34 = OrdersTotal() - 1 ; 臨_in_34 >= 0 ; 臨_in_34 = 臨_in_34 - 1)
    {
    if ( !(OrderSelect(臨_in_34,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
    
    if ( 臨_st_31 == "buy" && OrderType() == 0 && OrderTicket() > 臨_in_32 )
     {
     OrderOpenTime(); 
     OrderOpenPrice(); 
     臨_do_33 = OrderLots();
     臨_in_32 = OrderTicket();
     }
    if ( 臨_st_31 != "sell" || OrderType() != 1 || OrderTicket() <= 臨_in_32 )   continue;
    OrderOpenTime(); 
    OrderOpenPrice(); 
    臨_do_33 = OrderLots();
    臨_in_32 = OrderTicket();
    }
   if ( 臨_st_30 == "Ticket" )
    {
    臨_do_35 = 臨_in_32;
    }
   else
    {
    if ( 臨_st_30 == "Lots" )
     {
     臨_do_35 = 臨_do_33;
     }
    else
     {
     臨_do_35 = 0.0;
    }}
   臨_in_36 = 臨_do_35;
   臨_st_37 = "Ticket";
   臨_st_38 = "buy";
   臨_in_39 = 0;
   臨_do_40 = 0.0;
   for (臨_in_41 = OrdersTotal() - 1 ; 臨_in_41 >= 0 ; 臨_in_41 = 臨_in_41 - 1)
    {
    if ( !(OrderSelect(臨_in_41,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
    
    if ( 臨_st_38 == "buy" && OrderType() == 0 && OrderTicket() > 臨_in_39 )
     {
     OrderOpenTime(); 
     OrderOpenPrice(); 
     臨_do_40 = OrderLots();
     臨_in_39 = OrderTicket();
     }
    if ( 臨_st_38 != "sell" || OrderType() != 1 || OrderTicket() <= 臨_in_39 )   continue;
    OrderOpenTime(); 
    OrderOpenPrice(); 
    臨_do_40 = OrderLots();
    臨_in_39 = OrderTicket();
    }
   if ( 臨_st_37 == "Ticket" )
    {
    臨_do_42 = 臨_in_39;
    }
   else
    {
    if ( 臨_st_37 == "Lots" )
     {
     臨_do_42 = 臨_do_40;
     }
    else
     {
     臨_do_42 = 0.0;
    }}
   }
   while(OrderCloseBy(臨_do_42,臨_in_36,0xFFFFFFFF));
   }
  lizong_7(0); 
  if ( ObjectFind(總_st_32) <  0 )
   {
   ObjectCreate(總_st_32,OBJ_LABEL,0,0,0.0,0,0.0,0,0.0); 
   ObjectSet(總_st_32,OBJPROP_CORNER,1.0); 
   ObjectSet(總_st_32,OBJPROP_YDISTANCE,260.0); 
   ObjectSet(總_st_32,OBJPROP_XDISTANCE,10.0); 
   ObjectSetText(總_st_32,"Spread: " + DoubleToString((Ask - Bid) / 總_do_30,1) + " pips",13,"Arial",總_ui_31); 
   }
  ObjectSetText(總_st_32,"Spread: " + DoubleToString((Ask - Bid) / 總_do_30,1) + " pips",0,NULL,0xFFFFFFFF); 
  WindowRedraw(); 
  WindowRedraw(); 
  }
 if ( Over == false )
  {
  if ( HomeopathyCloseAll == true )
   {
   臨_st_43 = "buy";
   臨_in_44 = 0;
   for (臨_in_45 = OrdersTotal() - 1 ; 臨_in_45 >= 0 ; 臨_in_45=臨_in_45 - 1)
    {
    if ( !(OrderSelect(臨_in_45,SELECT_BY_POS,MODE_TRADES)) || Symbol() != OrderSymbol() || OrderMagicNumber() != Magic || OrderComment() != "SS" )   continue;
    
    if ( 臨_st_43 == "buy" && OrderType() == 0 )
     {
     臨_in_44 = 臨_in_44 + 1;
     }
    if ( 臨_st_43 != "sell" || OrderType() != 1 )   continue;
    臨_in_44 = 臨_in_44 + 1;
    }
   if ( 臨_in_44 <  1 )
    {
    臨_st_46 = "sell";
    臨_in_47 = 0;
    for (臨_in_48 = OrdersTotal() - 1 ; 臨_in_48 >= 0 ; 臨_in_48=臨_in_48 - 1)
     {
     if ( !(OrderSelect(臨_in_48,SELECT_BY_POS,MODE_TRADES)) || Symbol() != OrderSymbol() || OrderMagicNumber() != Magic || OrderComment() != "SS" )   continue;
     
     if ( 臨_st_46 == "buy" && OrderType() == 0 )
      {
      臨_in_47 = 臨_in_47 + 1;
      }
     if ( 臨_st_46 != "sell" || OrderType() != 1 )   continue;
     臨_in_47 = 臨_in_47 + 1;
     }

   }}
  if ( ( 臨_in_47 < 1 || HomeopathyCloseAll == false ) && 子_do_4>MaxLossCloseAll && 子_do_3>MaxLossCloseAll )
   {
   ObjectSetText("Char.op",CharToString(251),總_in_5 + 2,"Wingdings",Silver); 
   if ( ( ( Profit == true && 子_do_4>StopProfit * 子_in_8 ) || (Profit == false && 子_do_4>StopProfit) ) )
    {
    Print("Buy Profit ",子_do_4); 
    lizong_7(1); 
    return(0); 
    }
   if ( ( ( Profit == true && 子_do_3>StopProfit * 子_in_9 ) || (Profit == false && 子_do_3>StopProfit) ) )
    {
    Print("Sell Profit ",子_do_3); 
    lizong_7(-1); 
    return(0); 
   }}
  if ( HomeopathyCloseAll == true )
   {
   臨_st_49 = "buy";
   臨_in_50 = 0;
   for (臨_in_51 = OrdersTotal() - 1 ; 臨_in_51 >= 0 ; 臨_in_51=臨_in_51 - 1)
    {
    if ( !(OrderSelect(臨_in_51,SELECT_BY_POS,MODE_TRADES)) || Symbol() != OrderSymbol() || OrderMagicNumber() != Magic || OrderComment() != "SS" )   continue;
    
    if ( 臨_st_49 == "buy" && OrderType() == 0 )
     {
     臨_in_50 = 臨_in_50 + 1;
     }
    if ( 臨_st_49 != "sell" || OrderType() != 1 )   continue;
    臨_in_50 = 臨_in_50 + 1;
    }

   臨_st_52 = "sell";
   臨_in_53 = 0;
   for (臨_in_54 = OrdersTotal() - 1 ; 臨_in_54 >= 0 ; 臨_in_54=臨_in_54 - 1)
    {
    if ( !(OrderSelect(臨_in_54,SELECT_BY_POS,MODE_TRADES)) || Symbol() != OrderSymbol() || OrderMagicNumber() != Magic || OrderComment() != "SS" )   continue;
    
    if ( 臨_st_52 == "buy" && OrderType() == 0 )
     {
     臨_in_53 = 臨_in_53 + 1;
     }
    if ( 臨_st_52 != "sell" || OrderType() != 1 )   continue;
    臨_in_53 = 臨_in_53 + 1;
    }
   if ( ( 臨_in_50 > 0 || 臨_in_53 > 0 ) && 子_do_4 + 子_do_3>=CloseAll )
    {
    臨_st_55 = "Ticket";
    臨_st_56 = "sell";
    臨_in_57 = 0;
    臨_do_58 = 0.0;
    for (臨_in_59 = OrdersTotal() - 1 ; 臨_in_59 >= 0 ; 臨_in_59 = 臨_in_59 - 1)
     {
     if ( !(OrderSelect(臨_in_59,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
     
     if ( 臨_st_56 == "buy" && OrderType() == 0 && OrderTicket() > 臨_in_57 )
      {
      OrderOpenTime(); 
      OrderOpenPrice(); 
      臨_do_58 = OrderLots();
      臨_in_57 = OrderTicket();
      }
     if ( 臨_st_56 != "sell" || OrderType() != 1 || OrderTicket() <= 臨_in_57 )   continue;
     OrderOpenTime(); 
     OrderOpenPrice(); 
     臨_do_58 = OrderLots();
     臨_in_57 = OrderTicket();
     }
    if ( 臨_st_55 == "Ticket" )
     {
     臨_do_60 = 臨_in_57;
     }
    else
     {
     if ( 臨_st_55 == "Lots" )
      {
      臨_do_60 = 臨_do_58;
      }
     else
      {
      臨_do_60 = 0.0;
     }}
    臨_in_61 = 臨_do_60;
    臨_st_62 = "Ticket";
    臨_st_63 = "buy";
    臨_in_64 = 0;
    臨_do_65 = 0.0;
    for (臨_in_66 = OrdersTotal() - 1 ; 臨_in_66 >= 0 ; 臨_in_66 = 臨_in_66 - 1)
     {
     if ( !(OrderSelect(臨_in_66,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
     
     if ( 臨_st_63 == "buy" && OrderType() == 0 && OrderTicket() > 臨_in_64 )
      {
      OrderOpenTime(); 
      OrderOpenPrice(); 
      臨_do_65 = OrderLots();
      臨_in_64 = OrderTicket();
      }
     if ( 臨_st_63 != "sell" || OrderType() != 1 || OrderTicket() <= 臨_in_64 )   continue;
     OrderOpenTime(); 
     OrderOpenPrice(); 
     臨_do_65 = OrderLots();
     臨_in_64 = OrderTicket();
     }
    if ( 臨_st_62 == "Ticket" )
     {
     臨_do_67 = 臨_in_64;
     }
    else
     {
     if ( 臨_st_62 == "Lots" )
      {
      臨_do_67 = 臨_do_65;
      }
     else
      {
      臨_do_67 = 0.0;
     }}
     if(OrderCloseBy(臨_do_67,臨_in_61,0xFFFFFFFF)){
    do
     {
     臨_st_68 = "Ticket";
     臨_st_69 = "sell";
     臨_in_70 = 0;
     臨_do_71 = 0.0;
     for (臨_in_72 = OrdersTotal() - 1 ; 臨_in_72 >= 0 ; 臨_in_72 = 臨_in_72 - 1)
      {
      if ( !(OrderSelect(臨_in_72,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
      
      if ( 臨_st_69 == "buy" && OrderType() == 0 && OrderTicket() > 臨_in_70 )
       {
       OrderOpenTime(); 
       OrderOpenPrice(); 
       臨_do_71 = OrderLots();
       臨_in_70 = OrderTicket();
       }
      if ( 臨_st_69 != "sell" || OrderType() != 1 || OrderTicket() <= 臨_in_70 )   continue;
      OrderOpenTime(); 
      OrderOpenPrice(); 
      臨_do_71 = OrderLots();
      臨_in_70 = OrderTicket();
      }
     if ( 臨_st_68 == "Ticket" )
      {
      臨_do_73 = 臨_in_70;
      }
     else
      {
      if ( 臨_st_68 == "Lots" )
       {
       臨_do_73 = 臨_do_71;
       }
      else
       {
       臨_do_73 = 0.0;
      }}
     臨_in_74 = 臨_do_73;
     臨_st_75 = "Ticket";
     臨_st_76 = "buy";
     臨_in_77 = 0;
     臨_do_78 = 0.0;
     for (臨_in_79 = OrdersTotal() - 1 ; 臨_in_79 >= 0 ; 臨_in_79 = 臨_in_79 - 1)
      {
      if ( !(OrderSelect(臨_in_79,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
      
      if ( 臨_st_76 == "buy" && OrderType() == 0 && OrderTicket() > 臨_in_77 )
       {
       OrderOpenTime(); 
       OrderOpenPrice(); 
       臨_do_78 = OrderLots();
       臨_in_77 = OrderTicket();
       }
      if ( 臨_st_76 != "sell" || OrderType() != 1 || OrderTicket() <= 臨_in_77 )   continue;
      OrderOpenTime(); 
      OrderOpenPrice(); 
      臨_do_78 = OrderLots();
      臨_in_77 = OrderTicket();
      }
     if ( 臨_st_75 == "Ticket" )
      {
      臨_do_80 = 臨_in_77;
      }
     else
      {
      if ( 臨_st_75 == "Lots" )
       {
       臨_do_80 = 臨_do_78;
       }
      else
       {
       臨_do_80 = 0.0;
      }}
     }
     while(OrderCloseBy(臨_do_80,臨_in_74,0xFFFFFFFF));
     }
    lizong_7(0); 
    if ( NextTime > 0 )
     {
     總_da_9=TimeCurrent() + NextTime;
     }
    return(0); 
   }}
  if ( 子_do_4 + 子_do_3>=CloseAll && ( 子_do_4<=MaxLossCloseAll || 子_do_3<=MaxLossCloseAll ) )
   {
   臨_st_81 = "Ticket";
   臨_st_82 = "sell";
   臨_in_83 = 0;
   臨_do_84 = 0.0;
   for (臨_in_85 = OrdersTotal() - 1 ; 臨_in_85 >= 0 ; 臨_in_85 = 臨_in_85 - 1)
    {
    if ( !(OrderSelect(臨_in_85,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
    
    if ( 臨_st_82 == "buy" && OrderType() == 0 && OrderTicket() > 臨_in_83 )
     {
     OrderOpenTime(); 
     OrderOpenPrice(); 
     臨_do_84 = OrderLots();
     臨_in_83 = OrderTicket();
     }
    if ( 臨_st_82 != "sell" || OrderType() != 1 || OrderTicket() <= 臨_in_83 )   continue;
    OrderOpenTime(); 
    OrderOpenPrice(); 
    臨_do_84 = OrderLots();
    臨_in_83 = OrderTicket();
    }
   if ( 臨_st_81 == "Ticket" )
    {
    臨_do_86 = 臨_in_83;
    }
   else
    {
    if ( 臨_st_81 == "Lots" )
     {
     臨_do_86 = 臨_do_84;
     }
    else
     {
     臨_do_86 = 0.0;
    }}
   臨_in_87 = 臨_do_86;
   臨_st_88 = "Ticket";
   臨_st_89 = "buy";
   臨_in_90 = 0;
   臨_do_91 = 0.0;
   for (臨_in_92 = OrdersTotal() - 1 ; 臨_in_92 >= 0 ; 臨_in_92 = 臨_in_92 - 1)
    {
    if ( !(OrderSelect(臨_in_92,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
    
    if ( 臨_st_89 == "buy" && OrderType() == 0 && OrderTicket() > 臨_in_90 )
     {
     OrderOpenTime(); 
     OrderOpenPrice(); 
     臨_do_91 = OrderLots();
     臨_in_90 = OrderTicket();
     }
    if ( 臨_st_89 != "sell" || OrderType() != 1 || OrderTicket() <= 臨_in_90 )   continue;
    OrderOpenTime(); 
    OrderOpenPrice(); 
    臨_do_91 = OrderLots();
    臨_in_90 = OrderTicket();
    }
   if ( 臨_st_88 == "Ticket" )
    {
    臨_do_93 = 臨_in_90;
    }
   else
    {
    if ( 臨_st_88 == "Lots" )
     {
     臨_do_93 = 臨_do_91;
     }
    else
     {
     臨_do_93 = 0.0;
    }}
    if(OrderCloseBy(臨_do_93,臨_in_87,0xFFFFFFFF)){
   do
    {
    臨_st_94 = "Ticket";
    臨_st_95 = "sell";
    臨_in_96 = 0;
    臨_do_97 = 0.0;
    for (臨_in_98 = OrdersTotal() - 1 ; 臨_in_98 >= 0 ; 臨_in_98 = 臨_in_98 - 1)
     {
     if ( !(OrderSelect(臨_in_98,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
     
     if ( 臨_st_95 == "buy" && OrderType() == 0 && OrderTicket() > 臨_in_96 )
      {
      OrderOpenTime(); 
      OrderOpenPrice(); 
      臨_do_97 = OrderLots();
      臨_in_96 = OrderTicket();
      }
     if ( 臨_st_95 != "sell" || OrderType() != 1 || OrderTicket() <= 臨_in_96 )   continue;
     OrderOpenTime(); 
     OrderOpenPrice(); 
     臨_do_97 = OrderLots();
     臨_in_96 = OrderTicket();
     }
    if ( 臨_st_94 == "Ticket" )
     {
     臨_do_99 = 臨_in_96;
     }
    else
     {
     if ( 臨_st_94 == "Lots" )
      {
      臨_do_99 = 臨_do_97;
      }
     else
      {
      臨_do_99 = 0.0;
     }}
    臨_in_100 = 臨_do_99;
    臨_st_101 = "Ticket";
    臨_st_102 = "buy";
    臨_in_103 = 0;
    臨_do_104 = 0.0;
    for (臨_in_105 = OrdersTotal() - 1 ; 臨_in_105 >= 0 ; 臨_in_105 = 臨_in_105 - 1)
     {
     if ( !(OrderSelect(臨_in_105,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
     
     if ( 臨_st_102 == "buy" && OrderType() == 0 && OrderTicket() > 臨_in_103 )
      {
      OrderOpenTime(); 
      OrderOpenPrice(); 
      臨_do_104 = OrderLots();
      臨_in_103 = OrderTicket();
      }
     if ( 臨_st_102 != "sell" || OrderType() != 1 || OrderTicket() <= 臨_in_103 )   continue;
     OrderOpenTime(); 
     OrderOpenPrice(); 
     臨_do_104 = OrderLots();
     臨_in_103 = OrderTicket();
     }
    if ( 臨_st_101 == "Ticket" )
     {
     臨_do_106 = 臨_in_103;
     }
    else
     {
     if ( 臨_st_101 == "Lots" )
      {
      臨_do_106 = 臨_do_104;
      }
     else
      {
      臨_do_106 = 0.0;
     }}
    }
    while(OrderCloseBy(臨_do_106,臨_in_100,0xFFFFFFFF));
    }
   lizong_7(0); 
   if ( NextTime > 0 )
    {
    總_da_9=TimeCurrent() + NextTime;
    }
   return(0); 
  }}
 if ( StopLoss!=0.0 && 子_do_4 + 子_do_3<=StopLoss )
  {
  Print("Buy Loss ",子_do_4); 
  Print("Sell Loss ",子_do_3); 
  lizong_7(0); 
  if ( NextTime > 0 )
   {
   總_da_9=TimeCurrent() + NextTime;
   }
  return(0); 
  }
 if ( 子_do_4<=MaxLoss )
  {
  Comment("Buy"); 
  ObjectSetText("Char.b",CharToString(225) + CharToString(251),總_in_5,"Wingdings",Red); 
  }
 else
  {
  ObjectSetText("Char.b",CharToString(233),總_in_5,"Wingdings",Lime); 
  }
 if ( 子_do_3<=MaxLoss )
  {
  Comment("Sell"); 
  ObjectSetText("Char.s",CharToString(226) + CharToString(251),總_in_5,"Wingdings",Red); 
  }
 else
  {
  ObjectSetText("Char.s",CharToString(234),總_in_5,"Wingdings",Lime); 
  }
 if ( iOpen(Symbol(),1,0)>iOpen(Symbol(),1,1) )
  {
  總_in_40 = 總_in_38 ;
  }
 if ( iOpen(Symbol(),1,0)<iOpen(Symbol(),1,1) )
  {
  總_in_40 = 總_in_39 ;
  }
 if ( iClose(Symbol(),1,0)>iClose(Symbol(),1,1) )
  {
  總_in_40 = 總_in_42 ;
  }
 if ( iClose(Symbol(),1,0)<iClose(Symbol(),1,1) )
  {
  總_in_40 = 總_in_43 ;
  }
 子_do_28 = (Ask - Bid) / Point() ;
 子_st_29 = Symbol() + ": " + DoubleToString(子_do_28,1) + " pips" ;
 ObjectCreate(總_st_32,OBJ_LABEL,0,0,0.0,0,0.0,0,0.0); 
 ObjectSet(總_st_32,OBJPROP_CORNER,1.0); 
 ObjectSet(總_st_32,OBJPROP_YDISTANCE,340.0); 
 ObjectSet(總_st_32,OBJPROP_XDISTANCE,10.0); 
 ObjectSetText(總_st_32,子_st_29,13,"Arial",總_ui_31); 
 子_do_30 = AccountLeverage() ;
 子_st_31 = "Lever: " + DoubleToString(子_do_30,0) + " multi" ;
 ObjectCreate(總_st_44,OBJ_LABEL,0,0,0.0,0,0.0,0,0.0); 
 ObjectSet(總_st_44,OBJPROP_CORNER,1.0); 
 ObjectSet(總_st_44,OBJPROP_YDISTANCE,320.0); 
 ObjectSet(總_st_44,OBJPROP_XDISTANCE,10.0); 
 ObjectSetText(總_st_44,子_st_31,13,"Arial",總_ui_31); 
 if ( CloseBuySell == 1 )
  {
  子_do_32 = lizong_10(0,Magic,1,總_in_28) - lizong_10(0,Magic,2,總_in_29) ;
  if ( 總_do_23<子_do_32 )
   {
   總_do_23 = 子_do_32 ;
   }
  if ( 總_do_23>0.0 && 子_do_32>0.0 && 總_do_23>0.0 )
   {
   臨_in_107 = 1;
   臨_in_108 = Magic;
   臨_in_109 = 0;
   臨_do_110 = 0.0;
   臨_do_111 = 0.0;
   for (臨_in_112 = OrdersTotal() - 1 ; 臨_in_112 >= 0 ; 臨_in_112 = 臨_in_112 - 1)
    {
    if ( !(OrderSelect(臨_in_112,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || ( OrderMagicNumber()  !=  臨_in_108 && 臨_in_108 != -1 ) || ( OrderType()  !=  臨_in_109 && 臨_in_109 != -100 ) )   continue;
    
    if ( 臨_in_107 == 1 && 臨_do_111<OrderProfit() )
     {
     臨_do_111 = OrderProfit();
     臨_do_110 = OrderLots();
     }
    if ( 臨_in_107 != 2 || ( !(臨_do_111>OrderProfit()) && !(臨_do_111==0.0) ) )   continue;
    臨_do_111 = OrderProfit();
    臨_do_110 = OrderLots();
    }
   if ( 子_do_5>臨_do_110 * 3.0 + 子_do_6 && 子_in_8 > 3 )
    {
    lizong_9(0,Magic,總_in_28,1); 
    lizong_9(0,Magic,總_in_29,2); 
    總_do_23 = 0.0 ;
    總_do_24 = 0.0 ;
   }}
  子_do_32 = lizong_10(1,Magic,1,總_in_28) - lizong_10(1,Magic,2,總_in_29) ;
  if ( 總_do_24<子_do_32 )
   {
   總_do_24 = 子_do_32 ;
   }
  if ( 總_do_24>0.0 && 子_do_32>0.0 && 總_do_24>0.0 )
   {
   臨_in_113 = 1;
   臨_in_114 = Magic;
   臨_in_115 = 1;
   臨_do_116 = 0.0;
   臨_do_117 = 0.0;
   for (臨_in_118 = OrdersTotal() - 1 ; 臨_in_118 >= 0 ; 臨_in_118 = 臨_in_118 - 1)
    {
    if ( !(OrderSelect(臨_in_118,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || ( OrderMagicNumber()  !=  臨_in_114 && 臨_in_114 != -1 ) || ( OrderType()  !=  臨_in_115 && 臨_in_115 != -100 ) )   continue;
    
    if ( 臨_in_113 == 1 && 臨_do_117<OrderProfit() )
     {
     臨_do_117 = OrderProfit();
     臨_do_116 = OrderLots();
     }
    if ( 臨_in_113 != 2 || ( !(臨_do_117>OrderProfit()) && !(臨_do_117==0.0) ) )   continue;
    臨_do_117 = OrderProfit();
    臨_do_116 = OrderLots();
    }
   if ( 子_do_6>臨_do_116 * 3.0 + 子_do_5 && 子_in_9 > 3 )
    {
    lizong_9(1,Magic,總_in_28,1); 
    lizong_9(1,Magic,總_in_29,2); 
    總_do_23 = 0.0 ;
    總_do_24 = 0.0 ;
  }}}
 if ( ( ( Money!=0.0 && 子_do_39>Money ) || Money==0.0 ) )
  {
  子_bo_34 = true ;
  }
 if ( Money!=0.0 && 子_do_39<=Money )
  {
  子_bo_34 = false ;
  }

 if ( ( ( OpenMode == 1 && 總_da_62 != iTime(NULL,TimeZone,0) ) || OpenMode == 2 || OpenMode == 3 ) )
  {  
  if ( 子_in_10 == 0 && 子_do_4>MaxLoss && 總_bo_1 )
   {
   if ( 子_in_8 == 0 )
    {
    子_do_25 = NormalizeDouble(FirstStep * Point() + Ask,Digits()) ;
    }
   else
    {
    if ( 子_bo_34 )
     {
     子_do_25 = NormalizeDouble(MinDistance * Point() + Ask,Digits()) ;
     }
    if ( 子_bo_34 == false && Money!=0.0 )
     {
     子_do_25 = NormalizeDouble(TwoMinDistance * Point() + Ask,Digits()) ;
     }
    if ( 子_do_25<NormalizeDouble(子_do_16 - Step * Point(),Digits()) && 子_bo_34 )
     {
     子_do_25 = NormalizeDouble(Step * Point() + Ask,Digits()) ;
     }
    if ( 子_do_25<NormalizeDouble(子_do_16 - TwoStep * Point(),Digits()) && 子_bo_34 == false && Money!=0.0 )
     {
     子_do_25 = NormalizeDouble(TwoStep * Point() + Ask,Digits()) ;
    }}
   if ( ( 子_in_8 == 0 || ( 子_do_15!=0.0 && 子_do_25>=NormalizeDouble(Step * Point() + 子_do_15,Digits()) && 總_bo_11 && 子_bo_34 ) || ( 子_do_15!=0.0 && 子_do_25>=NormalizeDouble(TwoStep * Point() + 子_do_15,Digits()) && 總_bo_11 && 子_bo_34 == false && Money!=0.0 ) || ( 子_do_16!=0.0 && 子_do_25<=NormalizeDouble(子_do_16 - Step * Point(),Digits()) && 子_bo_34 ) || ( 子_do_16!=0.0 && 子_do_25<=NormalizeDouble(子_do_16 - TwoStep * Point(),Digits()) && 子_bo_34 == false && Money!=0.0 ) || (Homeopathy && 子_do_15!=0.0 && 子_do_25>=NormalizeDouble(Step * Point() + 子_do_15,Digits()) && 子_do_5==子_do_6) ) )
    {
    if ( 子_in_8 == 0 )
     {
     子_do_26 = lot ;
     }
    else
     {
     子_do_26 = NormalizeDouble(lot * MathPow(K_Lot,子_in_8) + 子_in_8 * PlusLot,DigitsLot) ;
     }
    if ( 子_do_26>Maxlot )
     {
     子_do_26 = Maxlot ;
     }
    // ================== 在开单条件中加入回撤停止加仓标志 ==================
    if ( ( ( 子_do_26 * 2.0<AccountFreeMargin() / MarketInfo(Symbol(),32) && 子_in_8 > 0 ) || 總_bo_10 ) && !總_bo_drawdownStop )
     {
     臨_da_119 = 0;
     if ( IsTesting() )
      {
      臨_da_119 = TimeCurrent();
      }
     else
      {
      臨_da_119 = TimeLocal();
      }
     總_da_63 = StringToTime(StringConcatenate(TimeYear(臨_da_119),".",TimeMonth(臨_da_119),".",TimeDay(臨_da_119)," ",EA_StartTime)) ;
     總_da_64 = StringToTime(StringConcatenate(TimeYear(臨_da_119),".",TimeMonth(臨_da_119),".",TimeDay(臨_da_119)," ",EA_StopTime)) ;
     if ( 總_da_63 <  總_da_64 && ( 臨_da_119 < 總_da_63 || 臨_da_119 > 總_da_64 ) )
      {
      臨_bo_120 = false;
      }
     else
      {
      if ( 總_da_63 > 總_da_64 && 臨_da_119 <  總_da_63 && 臨_da_119 > 總_da_64 )
       {
       臨_bo_120 = false;
       }
      else
       {
       臨_bo_120 = true;
      }}
     
     臨_da_121 = 0;
     if ( 臨_bo_120 )
      {
      if ( IsTesting() )
       {
       臨_da_121 = TimeCurrent();
       }
      else
       {
       臨_da_121 = TimeLocal();
       }
      總_da_65 = StringToTime(StringConcatenate(TimeYear(臨_da_121),".",TimeMonth(臨_da_121),".",TimeDay(臨_da_121)," ",Limit_StartTime)) ;
      總_da_66 = StringToTime(StringConcatenate(TimeYear(臨_da_121),".",TimeMonth(臨_da_121),".",TimeDay(臨_da_121)," ",Limit_StopTime)) ;
      if ( 總_da_65 <  總_da_66 && ( 臨_da_121 < 總_da_63 || 臨_da_121 > 總_da_66 ) )
       {
       ObjectDelete("HLINE_LONG"); 
       ObjectDelete("HLINE_SHORT"); 
       ObjectDelete("HLINE_LONGII"); 
       ObjectDelete("HLINE_SHORTII"); 
       臨_bo_122 = false;
       }
      else
       {
       if ( 總_da_65 > 總_da_66 && 臨_da_121 <  總_da_65 && 臨_da_121 > 總_da_66 )
        {
        ObjectDelete("HLINE_LONG"); 
        ObjectDelete("HLINE_SHORT"); 
        ObjectDelete("HLINE_LONGII"); 
        ObjectDelete("HLINE_SHORTII"); 
        臨_bo_122 = false;
        }
       else
        {
        臨_bo_122 = true;
       }}

      臨_da_123 = 0;
      if ( IsTesting() )
       {
       臨_da_123 = TimeCurrent();
       }
      else
       {
       臨_da_123 = TimeLocal();
       }
      總_da_65 = StringToTime(StringConcatenate(TimeYear(臨_da_123),".",TimeMonth(臨_da_123),".",TimeDay(臨_da_123)," ",Limit_StartTime)) ;
      總_da_66 = StringToTime(StringConcatenate(TimeYear(臨_da_123),".",TimeMonth(臨_da_123),".",TimeDay(臨_da_123)," ",Limit_StopTime)) ;
      
      if ( 總_da_65 <  總_da_66 && ( 臨_da_123 < 總_da_63 || 臨_da_123 > 總_da_66 ) )
       {
       ObjectDelete("HLINE_LONG"); 
       ObjectDelete("HLINE_SHORT"); 
       ObjectDelete("HLINE_LONGII"); 
       ObjectDelete("HLINE_SHORTII"); 
       臨_bo_124 = false;
       }
      else
       {
       if ( 總_da_65 > 總_da_66 && 臨_da_123 <  總_da_65 && 臨_da_123 > 總_da_66 )
        {
        ObjectDelete("HLINE_LONG"); 
        ObjectDelete("HLINE_SHORT"); 
        ObjectDelete("HLINE_LONGII"); 
        ObjectDelete("HLINE_SHORTII"); 
        臨_bo_124 = false;
        }
       else
        {
        臨_bo_124 = true;
       }}
      if ( !(臨_bo_124) )
       {
       臨_da_125 = 0;
       if ( IsTesting() )
        {
        臨_da_125 = TimeCurrent();
        }
       else
        {
        臨_da_125 = TimeLocal();
        }
       總_da_65 = StringToTime(StringConcatenate(TimeYear(臨_da_125),".",TimeMonth(臨_da_125),".",TimeDay(臨_da_125)," ",Limit_StartTime)) ;
       總_da_66 = StringToTime(StringConcatenate(TimeYear(臨_da_125),".",TimeMonth(臨_da_125),".",TimeDay(臨_da_125)," ",Limit_StopTime)) ;
       if ( 總_da_65 <  總_da_66 && ( 臨_da_125 < 總_da_63 || 臨_da_125 > 總_da_66 ) )
        {
        ObjectDelete("HLINE_LONG"); 
        ObjectDelete("HLINE_SHORT"); 
        ObjectDelete("HLINE_LONGII"); 
        ObjectDelete("HLINE_SHORTII"); 
        臨_bo_126 = false;
        }
       else
        {
        if ( 總_da_65 > 總_da_66 && 臨_da_125 <  總_da_65 && 臨_da_125 > 總_da_66 )
         {
         ObjectDelete("HLINE_LONG"); 
         ObjectDelete("HLINE_SHORT"); 
         ObjectDelete("HLINE_LONGII"); 
         ObjectDelete("HLINE_SHORTII"); 
         臨_bo_126 = false;
         }
        else
         {
         臨_bo_126 = true;
        }}
     // if ( (   (臨_bo_126 && 子_in_8 >= 1) ) )
     //  {
        

       臨_da_127 = 0;
       if ( IsTesting() )
        {
        臨_da_127 = TimeCurrent();
        }
       else
        {
        臨_da_127 = TimeLocal();
        }
       總_da_65 = StringToTime(StringConcatenate(TimeYear(臨_da_127),".",TimeMonth(臨_da_127),".",TimeDay(臨_da_127)," ",Limit_StartTime)) ;
       總_da_66 = StringToTime(StringConcatenate(TimeYear(臨_da_127),".",TimeMonth(臨_da_127),".",TimeDay(臨_da_127)," ",Limit_StopTime)) ;
       if ( 總_da_65 <  總_da_66 && ( 臨_da_127 < 總_da_63 || 臨_da_127 > 總_da_66 ) )
        {
        ObjectDelete("HLINE_LONG"); 
        ObjectDelete("HLINE_SHORT"); 
        ObjectDelete("HLINE_LONGII"); 
        ObjectDelete("HLINE_SHORTII"); 
        臨_bo_128 = false;
        }
       else
        {
        if ( 總_da_65 > 總_da_66 && 臨_da_127 <  總_da_65 && 臨_da_127 > 總_da_66 )
         {
         ObjectDelete("HLINE_LONG"); 
         ObjectDelete("HLINE_SHORT"); 
         ObjectDelete("HLINE_LONGII"); 
         ObjectDelete("HLINE_SHORTII"); 
         臨_bo_128 = false;
         }
        else
         {
         臨_bo_128 = true;
        }}

       臨_da_129 = 0;
       if ( IsTesting() )
        {
        臨_da_129 = TimeCurrent();
        }
       else
        {
        臨_da_129 = TimeLocal();
        }
       總_da_65 = StringToTime(StringConcatenate(TimeYear(臨_da_129),".",TimeMonth(臨_da_129),".",TimeDay(臨_da_129)," ",Limit_StartTime)) ;
       總_da_66 = StringToTime(StringConcatenate(TimeYear(臨_da_129),".",TimeMonth(臨_da_129),".",TimeDay(臨_da_129)," ",Limit_StopTime)) ;
       if ( 總_da_65 <  總_da_66 && ( 臨_da_129 < 總_da_63 || 臨_da_129 > 總_da_66 ) )
        {
        ObjectDelete("HLINE_LONG"); 
        ObjectDelete("HLINE_SHORT"); 
        ObjectDelete("HLINE_LONGII"); 
        ObjectDelete("HLINE_SHORTII"); 
        臨_bo_130 = false;
        }
       else
        {
        if ( 總_da_65 > 總_da_66 && 臨_da_129 <  總_da_65 && 臨_da_129 > 總_da_66 )
         {
         ObjectDelete("HLINE_LONG"); 
         ObjectDelete("HLINE_SHORT"); 
         ObjectDelete("HLINE_LONGII"); 
         ObjectDelete("HLINE_SHORTII"); 
         臨_bo_130 = false;
         }
        else
         {
         臨_bo_130 = true;
        }}
        }
       // Print("總_da_65=",總_da_65,"  總_da_66=",總_da_66,"  臨_da_123=",臨_da_123,"  總_da_63=",總_da_63,"  臨_da_123=",臨_da_123);
       if ( ( On_top_of_this_price_not_Buy_order==0.0 || ( 臨_bo_128 && 子_in_8 >= 1 && 子_do_25<On_top_of_this_price_not_Buy_order ) || 子_in_8 == 0 || !(臨_bo_130) ) )
        {
        臨_in_131 = 0;
        臨_in_132 = Magic;
        臨_in_133 = 0;
        臨_in_134 = 0;
        for (臨_in_135 = OrdersTotal() - 1 ; 臨_in_135 >= 0 ; 臨_in_135=臨_in_135 - 1)
         {
         if ( !(OrderSelect(臨_in_135,SELECT_BY_POS,MODE_TRADES)) || Symbol() != OrderSymbol() || OrderMagicNumber() != 臨_in_132 || OrderTicket() <= 臨_in_134 || OrderType() != 臨_in_131 )   continue;
         臨_in_134 = OrderTicket();
         臨_in_133 = OrderOpenTime();
         }
        if ( ( ( TimeCurrent() - 臨_in_133 >= sleep && OpenMode == 2 ) || OpenMode == 3 || OpenMode == 1 ) )
         {
         if ( ( ( 子_do_15!=0.0 && 子_do_25>=NormalizeDouble(Step * Point() + 子_do_15,Digits()) && 總_bo_11 && 子_bo_34 ) || ( 子_do_15!=0.0 && 子_do_25>=NormalizeDouble(TwoStep * Point() + 子_do_15,Digits()) && 總_bo_11 && 子_bo_34 == false && Money!=0.0 ) || (Homeopathy && 子_do_15!=0.0 && 子_do_25>=NormalizeDouble(Step * Point() + 子_do_15,Digits()) && 子_do_5==子_do_6) ) )
          {
          總_in_69 = OrderSend(Symbol(),OP_BUYSTOP,子_do_26,子_do_25,總_in_22,0.0,0.0,"SS",Magic,0,Blue) ;
          if ( 總_in_69 > 0 )
           {
           Print(Symbol() + "開單成功，訂單編號:" + DoubleToString(總_in_69,0)); 
           }
          else
           {
           Print(Symbol() + "開單失敗"); 
          }}
         else
          {
          總_in_69 = OrderSend(Symbol(),OP_BUYSTOP,子_do_26,子_do_25,總_in_22,0.0,0.0,"NN",Magic,0,Blue) ;
          if ( 總_in_69 > 0 )
           {
           Print(Symbol() + "開單成功，訂單編號:" + DoubleToString(總_in_69,0)); 
           }
          else
           {
           Print(Symbol() + "開單失敗"); 
      }}}}}}
     else
      {
      Comment("Lot ",DoubleToString(子_do_26,2)); 
    }}}
    
   if ( 子_in_11 == 0 && 子_do_3>MaxLoss && 總_bo_2 )
    {
    if ( 子_in_9 == 0 )
     {
     子_do_25 = NormalizeDouble(Bid - FirstStep * Point(),Digits()) ;
     }
    else
     {
     if ( 子_bo_34 )
      {
      子_do_25 = NormalizeDouble(Bid - MinDistance * Point(),Digits()) ;
      }
     if ( 子_bo_34 == false )
      {
      子_do_25 = NormalizeDouble(Bid - TwoMinDistance * Point(),Digits()) ;
      }
     if ( 子_do_25<NormalizeDouble(Step * Point() + 子_do_17,Digits()) && 子_bo_34 )
      {
      子_do_25 = NormalizeDouble(Bid - Step * Point(),Digits()) ;
      }
     if ( 子_do_25<NormalizeDouble(TwoStep * Point() + 子_do_17,Digits()) && 子_bo_34 == false && Money!=0.0 )
      {
      子_do_25 = NormalizeDouble(Bid - TwoStep * Point(),Digits()) ;
     }}
    if ( ( 子_in_9 == 0 || ( 子_do_18!=0.0 && 子_do_25<=NormalizeDouble(子_do_18 - Step * Point(),Digits()) && 總_bo_12 && 子_bo_34 ) || ( 子_do_18!=0.0 && 子_do_25<=NormalizeDouble(子_do_18 - TwoStep * Point(),Digits()) && 總_bo_12 && 子_bo_34 == false && Money!=0.0 ) || ( 子_do_17!=0.0 && 子_do_25>=NormalizeDouble(Step * Point() + 子_do_17,Digits()) && 子_bo_34 ) || ( 子_do_17!=0.0 && 子_do_25>=NormalizeDouble(TwoStep * Point() + 子_do_17,Digits()) && 子_bo_34 == false && Money!=0.0 ) || (Homeopathy && 子_do_18!=0.0 && 子_do_25<=NormalizeDouble(子_do_18 - Step * Point(),Digits()) && 子_do_5==子_do_6) ) )
     {
     if ( 子_in_9 == 0 )
      {
      子_do_26 = lot ;
      }
     else
      {
      子_do_26 = NormalizeDouble(lot * MathPow(K_Lot,子_in_9) + 子_in_9 * PlusLot,DigitsLot) ;
      }
     if ( 子_do_26>Maxlot )
      {
      子_do_26 = Maxlot ;
      }
     // ================== 在开单条件中加入回撤停止加仓标志 ==================
     if ( ( ( 子_do_26 * 2.0<AccountFreeMargin() / MarketInfo(Symbol(),32) && 子_in_9 > 0 ) || 總_bo_10 ) && !總_bo_drawdownStop )
      {
      臨_da_136 = 0;
      if ( IsTesting() )
       {
       臨_da_136 = TimeCurrent();
       }
      else
       {
       臨_da_136 = TimeLocal();
       }
      總_da_63 = StringToTime(StringConcatenate(TimeYear(臨_da_136),".",TimeMonth(臨_da_136),".",TimeDay(臨_da_136)," ",EA_StartTime)) ;
      總_da_64 = StringToTime(StringConcatenate(TimeYear(臨_da_136),".",TimeMonth(臨_da_136),".",TimeDay(臨_da_136)," ",EA_StopTime)) ;
      if ( 總_da_63 <  總_da_64 && ( 臨_da_136 < 總_da_63 || 臨_da_136 > 總_da_64 ) )
       {
       臨_bo_137 = false;
       }
      else
       {
       if ( 總_da_63 > 總_da_64 && 臨_da_136 <  總_da_63 && 臨_da_136 > 總_da_64 )
        {
        臨_bo_137 = false;
        }
       else
        {
        臨_bo_137 = true;
       }}

      臨_da_138 = 0;
      if ( 臨_bo_137 )
       {
       if ( IsTesting() )
        {
        臨_da_138 = TimeCurrent();
        }
       else
        {
        臨_da_138 = TimeLocal();
        }
       總_da_65 = StringToTime(StringConcatenate(TimeYear(臨_da_138),".",TimeMonth(臨_da_138),".",TimeDay(臨_da_138)," ",Limit_StartTime)) ;
       總_da_66 = StringToTime(StringConcatenate(TimeYear(臨_da_138),".",TimeMonth(臨_da_138),".",TimeDay(臨_da_138)," ",Limit_StopTime)) ;
       if ( 總_da_65 <  總_da_66 && ( 臨_da_138 < 總_da_63 || 臨_da_138 > 總_da_66 ) )
        {
        ObjectDelete("HLINE_LONG"); 
        ObjectDelete("HLINE_SHORT"); 
        ObjectDelete("HLINE_LONGII"); 
        ObjectDelete("HLINE_SHORTII"); 
        臨_bo_139 = false;
        }
       else
        {
        if ( 總_da_65 > 總_da_66 && 臨_da_138 <  總_da_65 && 臨_da_138 > 總_da_66 )
         {
         ObjectDelete("HLINE_LONG"); 
         ObjectDelete("HLINE_SHORT"); 
         ObjectDelete("HLINE_LONGII"); 
         ObjectDelete("HLINE_SHORTII"); 
         臨_bo_139 = false;
         }
        else
         {
         臨_bo_139 = true;
        }}

       臨_da_140 = 0;
       if ( IsTesting() )
        {
        臨_da_140 = TimeCurrent();
        }
       else
        {
        臨_da_140 = TimeLocal();
        }
       總_da_65 = StringToTime(StringConcatenate(TimeYear(臨_da_140),".",TimeMonth(臨_da_140),".",TimeDay(臨_da_140)," ",Limit_StartTime)) ;
       總_da_66 = StringToTime(StringConcatenate(TimeYear(臨_da_140),".",TimeMonth(臨_da_140),".",TimeDay(臨_da_140)," ",Limit_StopTime)) ;
       if ( 總_da_65 <  總_da_66 && ( 臨_da_140 < 總_da_63 || 臨_da_140 > 總_da_66 ) )
        {
        ObjectDelete("HLINE_LONG"); 
        ObjectDelete("HLINE_SHORT"); 
        ObjectDelete("HLINE_LONGII"); 
        ObjectDelete("HLINE_SHORTII"); 
        臨_bo_141 = false;
        }
       else
        {
        if ( 總_da_65 > 總_da_66 && 臨_da_140 <  總_da_65 && 臨_da_140 > 總_da_66 )
         {
         ObjectDelete("HLINE_LONG"); 
         ObjectDelete("HLINE_SHORT"); 
         ObjectDelete("HLINE_LONGII"); 
         ObjectDelete("HLINE_SHORTII"); 
         臨_bo_141 = false;
         }
        else
         {
         臨_bo_141 = true;
        }}
       if ( !(臨_bo_141) )
        {
        臨_da_142 = 0;
        if ( IsTesting() )
         {
         臨_da_142 = TimeCurrent();
         }
        else
         {
         臨_da_142 = TimeLocal();
         }
        總_da_65 = StringToTime(StringConcatenate(TimeYear(臨_da_142),".",TimeMonth(臨_da_142),".",TimeDay(臨_da_142)," ",Limit_StartTime)) ;
        總_da_66 = StringToTime(StringConcatenate(TimeYear(臨_da_142),".",TimeMonth(臨_da_142),".",TimeDay(臨_da_142)," ",Limit_StopTime)) ;
        if ( 總_da_65 <  總_da_66 && ( 臨_da_142 < 總_da_63 || 臨_da_142 > 總_da_66 ) )
         {
         ObjectDelete("HLINE_LONG"); 
         ObjectDelete("HLINE_SHORT"); 
         ObjectDelete("HLINE_LONGII"); 
         ObjectDelete("HLINE_SHORTII"); 
         臨_bo_143 = false;
         }
        else
         {
         if ( 總_da_65 > 總_da_66 && 臨_da_142 <  總_da_65 && 臨_da_142 > 總_da_66 )
          {
          ObjectDelete("HLINE_LONG"); 
          ObjectDelete("HLINE_SHORT"); 
          ObjectDelete("HLINE_LONGII"); 
          ObjectDelete("HLINE_SHORTII"); 
          臨_bo_143 = false;
          }
         else
          {
          臨_bo_143 = true;
         }}
       //if ( (   (臨_bo_143 && 子_in_9 >= 1) ) )
      //  {
         

        臨_da_144 = 0;
        if ( IsTesting() )
         {
         臨_da_144 = TimeCurrent();
         }
        else
         {
         臨_da_144 = TimeLocal();
         }
        總_da_65 = StringToTime(StringConcatenate(TimeYear(臨_da_144),".",TimeMonth(臨_da_144),".",TimeDay(臨_da_144)," ",Limit_StartTime)) ;
        總_da_66 = StringToTime(StringConcatenate(TimeYear(臨_da_144),".",TimeMonth(臨_da_144),".",TimeDay(臨_da_144)," ",Limit_StopTime)) ;
        if ( 總_da_65 <  總_da_66 && ( 臨_da_144 < 總_da_63 || 臨_da_144 > 總_da_66 ) )
         {
         ObjectDelete("HLINE_LONG"); 
         ObjectDelete("HLINE_SHORT"); 
         ObjectDelete("HLINE_LONGII"); 
         ObjectDelete("HLINE_SHORTII"); 
         臨_bo_145 = false;
         }
        else
         {
         if ( 總_da_65 > 總_da_66 && 臨_da_144 <  總_da_65 && 臨_da_144 > 總_da_66 )
          {
          ObjectDelete("HLINE_LONG"); 
          ObjectDelete("HLINE_SHORT"); 
          ObjectDelete("HLINE_LONGII"); 
          ObjectDelete("HLINE_SHORTII"); 
          臨_bo_145 = false;
          }
         else
          {
          臨_bo_145 = true;
         }}

        臨_da_146 = 0;
        if ( IsTesting() )
         {
         臨_da_146 = TimeCurrent();
         }
        else
         {
         臨_da_146 = TimeLocal();
         }
        總_da_65 = StringToTime(StringConcatenate(TimeYear(臨_da_146),".",TimeMonth(臨_da_146),".",TimeDay(臨_da_146)," ",Limit_StartTime)) ;
        總_da_66 = StringToTime(StringConcatenate(TimeYear(臨_da_146),".",TimeMonth(臨_da_146),".",TimeDay(臨_da_146)," ",Limit_StopTime)) ;
        if ( 總_da_65 <  總_da_66 && ( 臨_da_146 < 總_da_63 || 臨_da_146 > 總_da_66 ) )
         {
         ObjectDelete("HLINE_LONG"); 
         ObjectDelete("HLINE_SHORT"); 
         ObjectDelete("HLINE_LONGII"); 
         ObjectDelete("HLINE_SHORTII"); 
         臨_bo_147 = false;
         }
        else
         {
         if ( 總_da_65 > 總_da_66 && 臨_da_146 <  總_da_65 && 臨_da_146 > 總_da_66 )
          {
          ObjectDelete("HLINE_LONG"); 
          ObjectDelete("HLINE_SHORT"); 
          ObjectDelete("HLINE_LONGII"); 
          ObjectDelete("HLINE_SHORTII"); 
          臨_bo_147 = false;
          }
         else
          {
          臨_bo_147 = true;
         }}
         }
        // Print("總_da_65=",總_da_65,"  總_da_66=",總_da_66,"  臨_da_123=",臨_da_123,"  總_da_63=",總_da_63,"  臨_da_123=",臨_da_123);
        if ( ( On_under_of_this_price_not_Sell_order==0.0 || ( 臨_bo_145 && 子_in_9 >= 1 && 子_do_25>On_under_of_this_price_not_Sell_order ) || 子_in_9 == 0 || !(臨_bo_147) ) )
         {
         臨_in_148 = 1;
         臨_in_149 = Magic;
         臨_in_150 = 0;
         臨_in_151 = 0;
         for (臨_in_152 = OrdersTotal() - 1 ; 臨_in_152 >= 0 ; 臨_in_152=臨_in_152 - 1)
          {
          if ( !(OrderSelect(臨_in_152,SELECT_BY_POS,MODE_TRADES)) || Symbol() != OrderSymbol() || OrderMagicNumber() != 臨_in_149 || OrderTicket() <= 臨_in_151 || OrderType() != 臨_in_148 )   continue;
          臨_in_151 = OrderTicket();
          臨_in_150 = OrderOpenTime();
          }
         if ( ( ( TimeCurrent() - 臨_in_150 >= sleep && OpenMode == 2 ) || OpenMode == 3 || OpenMode == 1 ) )
          {
          if ( ( ( 子_do_18!=0.0 && 子_do_25<=NormalizeDouble(子_do_18 - Step * Point(),Digits()) && 總_bo_12 && 子_bo_34 ) || ( 子_do_18!=0.0 && 子_do_25<=NormalizeDouble(子_do_18 - TwoStep * Point(),Digits()) && 總_bo_12 && 子_bo_34 == false && Money!=0.0 ) || (Homeopathy && 子_do_18!=0.0 && 子_do_25<=NormalizeDouble(子_do_18 - Step * Point(),Digits()) && 子_do_5==子_do_6) ) )
           {
           總_in_69 = OrderSend(Symbol(),OP_SELLSTOP,子_do_26,子_do_25,總_in_22,0.0,0.0,"SS",Magic,0,Red) ;
           if ( 總_in_69 > 0 )
            {
            Print(Symbol() + "開單成功，訂單編號:" + DoubleToString(總_in_69,0)); 
            }
           else
            {
            Print(Symbol() + "開單失敗"); 
           }}
          else
           {
           總_in_69 = OrderSend(Symbol(),OP_SELLSTOP,子_do_26,子_do_25,總_in_22,0.0,0.0,"NN",Magic,0,Red) ;
           if ( 總_in_69 > 0 )
            {
            Print(Symbol() + "開單成功，訂單編號:" + DoubleToString(總_in_69,0)); 
            }
           else
            {
            Print(Symbol() + "開單失敗"); 
       }}}}}}
      else
       {
       Comment("Lot ",DoubleToString(子_do_26,2)); 
     }}}
    總_da_62 = iTime(NULL,TimeZone,0) ;
    }
   ObjectSetText("Balance",StringConcatenate("餘額 ",DoubleToString(AccountBalance(),2)),總_in_5,"Arial",總_ui_6); 
   ObjectSetText("Equity",StringConcatenate("淨值 ",DoubleToString(AccountEquity(),2)),總_in_5,"Arial",總_ui_6); 
   ObjectSetText("FreeMargin",StringConcatenate("可用保證金 ",DoubleToString(AccountFreeMargin(),2)),總_in_5,"Arial",總_ui_6); 
   子_do_33 = 子_do_4 + 子_do_3 ;
   if ( 子_do_5>0.0 )
    {
    if ( 子_do_4>0.0 )
     {
     臨_in_153 = 255;
     }
    else
     {
     臨_in_153 = 65280;
     }
    ObjectSetText("ProfitB",StringConcatenate("Buy ",子_in_8,"單 , ",DoubleToString(子_do_5,2),"手,  盈虧= ",DoubleToString(子_do_4,2)),總_in_5,"Arial",臨_in_153); 
    }
   else
    {
    ObjectSetText("ProfitB","",總_in_5,"Arial",Gray); 
    }
   if ( 子_do_6>0.0 )
    {
    if ( 子_do_3>0.0 )
     {
     臨_in_154 = 255;
     }
    else
     {
     臨_in_154 = 65280;
     }
    ObjectSetText("ProfitS",StringConcatenate("Sell ",子_in_9,"單 , ",DoubleToString(子_do_6,2),"手,  盈虧= ",DoubleToString(子_do_3,2)),總_in_5,"Arial",臨_in_154); 
    }
   else
    {
    ObjectSetText("ProfitS","",總_in_5,"Arial",Gray); 
    }
   if ( 子_do_6 + 子_do_5>0.0 )
    {
    if ( 子_do_33>0.0 )
     {
     臨_in_155 = 255;
     }
    else
     {
     臨_in_155 = 65280;
     }
    ObjectSetText("Profit",StringConcatenate("總盈虧= ",DoubleToString(子_do_33,2)),總_in_5,"Arial",臨_in_155); 
    }
   else
    {
    ObjectSetText("Profit","",總_in_5,"Arial",White); 
    }
   if ( 子_do_19!=0.0 && 總_bo_1 )
    {
    if ( 子_in_8 == 0 )
     {
     子_do_25 = NormalizeDouble(FirstStep * Point() + Ask,Digits()) ;
     }
    if ( 子_bo_34 && 子_in_8 > 0 )
     {
     子_do_25 = NormalizeDouble(MinDistance * Point() + Ask,Digits()) ;
     }
    if ( 子_bo_34 == false && 子_in_8 > 0 && Money!=0.0 )
     {
     子_do_25 = NormalizeDouble(TwoMinDistance * Point() + Ask,Digits()) ;
     }
    if ( NormalizeDouble(子_do_19 - StepTrallOrders * Point(),Digits())>子_do_25 && ( ( ( 子_do_25<=NormalizeDouble(子_do_16 - Step * Point(),Digits()) || 子_do_16==0.0 || ( 總_bo_11 && 子_in_8 == 0 ) || 子_do_25>=NormalizeDouble(Step * Point() + 子_do_15,Digits()) || 子_do_25<=NormalizeDouble(子_do_16 - Step * Point(),Digits()) ) && 子_bo_34 ) || (( 子_do_25<=NormalizeDouble(子_do_16 - TwoStep * Point(),Digits()) || 子_do_16==0.0 || ( 總_bo_11 && 子_in_8 == 0 ) || 子_do_25>=NormalizeDouble(TwoStep * Point() + 子_do_15,Digits()) || 子_do_25<=NormalizeDouble(子_do_16 - TwoStep * Point(),Digits()) ) && 子_bo_34 == false && Money!=0.0) ) )
     {
     if ( !(OrderModify(子_in_13,子_do_25,0.0,0.0,0,White)) )
      {
      Print("Error ",GetLastError(),"   Order Modify Buy   OOP ",子_do_19,"->",子_do_25); 
      }
     else
      {
      Print("Order Buy Modify   OOP ",子_do_2,"->",子_do_25); 
    }}}
   if ( 子_do_20!=0.0 && 總_bo_2 )
    {
    if ( 子_in_9 == 0 )
     {
     子_do_25 = NormalizeDouble(Bid - FirstStep * Point(),Digits()) ;
     }
    if ( 子_bo_34 && 子_in_9 > 0 )
     {
     子_do_25 = NormalizeDouble(Bid - MinDistance * Point(),Digits()) ;
     }
    if ( 子_bo_34 == false && 子_in_9 > 0 && Money!=0.0 )
     {
     子_do_25 = NormalizeDouble(Bid - TwoMinDistance * Point(),Digits()) ;
     }
    if ( NormalizeDouble(StepTrallOrders * Point() + 子_do_20,Digits())<子_do_25 && ( ( ( 子_do_25>=NormalizeDouble(Step * Point() + 子_do_17,Digits()) || 子_do_17==0.0 || ( 總_bo_12 && 子_in_9 == 0 ) || 子_do_25<=NormalizeDouble(子_do_18 - Step * Point(),Digits()) || 子_do_25>=NormalizeDouble(Step * Point() + 子_do_17,Digits()) ) && 子_bo_34 ) || (( 子_do_25>=NormalizeDouble(TwoStep * Point() + 子_do_17,Digits()) || 子_do_17==0.0 || ( 總_bo_12 && 子_in_9 == 0 ) || 子_do_25<=NormalizeDouble(子_do_18 - TwoStep * Point(),Digits()) || 子_do_25>=NormalizeDouble(TwoStep * Point() + 子_do_17,Digits()) ) && 子_bo_34 == false && Money!=0.0) ) )
     {
     if ( !(OrderModify(子_in_14,子_do_25,0.0,0.0,0,White)) )
      {
      Print("Error ",GetLastError(),"   Order Modify Sell   OOP ",子_do_20,"->",子_do_25); 
      }
     else
      {
      Print("Order Sell Modify   OOP ",子_do_2,"->",子_do_25); 
    }}}
   return(0); 
   }
//start
//---------------------  ----------------------------------------

   void OnChartEvent (const int 木_0,const long &木_1,const double &木_2,const string &木_3)
   {
 int         子_in_1;
 int         子_in_2;
 int         子_in_3;
 int         子_in_4;
 int         子_in_5;
 int         子_in_6;
 int         子_in_7;
 int         子_in_8;
 int         子_in_9;

//----------------------------
 string     臨_st_1;
 int        臨_in_2;
 int        臨_in_3;
 string     臨_st_4;
 int        臨_in_5;
 int        臨_in_6;
 string     臨_st_7;
 int        臨_in_8;
 int        臨_in_9;
 int        臨_in_10;
 string     臨_st_11;
 int        臨_in_12;
 int        臨_in_13;
 string     臨_st_14;
 string     臨_st_15;
 int        臨_in_16;
 double     臨_do_17;
 int        臨_in_18;
 double     臨_do_19;
 int        臨_in_20;
 string     臨_st_21;
 string     臨_st_22;
 int        臨_in_23;
 double     臨_do_24;
 int        臨_in_25;
 double     臨_do_26;
 string     臨_st_27;
 string     臨_st_28;
 int        臨_in_29;
 double     臨_do_30;
 int        臨_in_31;
 double     臨_do_32;
 int        臨_in_33;
 string     臨_st_34;
 string     臨_st_35;
 int        臨_in_36;
 double     臨_do_37;
 int        臨_in_38;
 double     臨_do_39;

 if ( 木_0 == 1 )
  {
  臨_st_1 = "buy";
  臨_in_2 = 0;
  for (臨_in_3 = OrdersTotal() - 1 ; 臨_in_3 >= 0 ; 臨_in_3 = 臨_in_3 - 1)
   {
   總_in_69 = OrderSelect(臨_in_3,SELECT_BY_POS,MODE_TRADES) ;
   if ( OrderSymbol() != Symbol() || OrderMagicNumber() != Magic || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
   
   if ( 臨_st_1 == "buy" && OrderType() == 0 )
    {
    臨_in_2 = 臨_in_2 + 1;
    }
   if ( 臨_st_1 == "sell" && OrderType() == 1 )
    {
    臨_in_2 = 臨_in_2 + 1;
    }
   if ( 臨_st_1 == "buystop" && OrderType() == 4 )
    {
    臨_in_2 = 臨_in_2 + 1;
    }
   if ( 臨_st_1 != "sellstop" || OrderType() != 5 )   continue;
   臨_in_2 = 臨_in_2 + 1;
   }
  if ( 臨_in_2 > 0 )
   {
   子_in_1 = 0 ;
   if ( 木_3 == "Button1" && 總_bo_34 == 1 )
    {
    子_in_2 = MessageBox("點擊確定(Y)表示將全部平多單!是否繼續?","友情提醒：",52) ;
    if ( 子_in_2 == 6 )
     {
     for (子_in_3 = OrdersTotal() - 1 ; 子_in_3 >= 0 ; 子_in_3 = 子_in_3 - 1)
      {
      總_in_69 = OrderSelect(子_in_3,SELECT_BY_POS,MODE_TRADES) ;
      if ( OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
      
      if ( OrderType() == 0 )
       {
       子_in_1 = OrderClose(OrderTicket(),OrderLots(),MarketInfo(OrderSymbol(),9),5,Red) ;
       }
      if ( OrderType() == 4 )
       {
       總_in_69 = OrderDelete(OrderTicket(),0xFFFFFFFF) ;
       }
      if ( 子_in_1 <= 0 )   continue;
      PlaySound("ok.wav"); 
      }
   }}}}
 if ( 木_0 == 1 )
  {
  臨_st_4 = "sell";
  臨_in_5 = 0;
  for (臨_in_6 = OrdersTotal() - 1 ; 臨_in_6 >= 0 ; 臨_in_6 = 臨_in_6 - 1)
   {
   總_in_69 = OrderSelect(臨_in_6,SELECT_BY_POS,MODE_TRADES) ;
   if ( OrderSymbol() != Symbol() || OrderMagicNumber() != Magic || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
   
   if ( 臨_st_4 == "buy" && OrderType() == 0 )
    {
    臨_in_5 = 臨_in_5 + 1;
    }
   if ( 臨_st_4 == "sell" && OrderType() == 1 )
    {
    臨_in_5 = 臨_in_5 + 1;
    }
   if ( 臨_st_4 == "buystop" && OrderType() == 4 )
    {
    臨_in_5 = 臨_in_5 + 1;
    }
   if ( 臨_st_4 != "sellstop" || OrderType() != 5 )   continue;
   臨_in_5 = 臨_in_5 + 1;
   }
  if ( 臨_in_5 > 0 )
   {
   子_in_4 = 0 ;
   if ( 木_3 == "Button2" && 總_bo_34 == 1 )
    {
    子_in_5 = MessageBox("點擊確定(Y)表示將全部平空單!是否繼續?","友情提醒：",52) ;
    if ( 子_in_5 == 6 )
     {
     for (子_in_6 = OrdersTotal() - 1 ; 子_in_6 >= 0 ; 子_in_6 = 子_in_6 - 1)
      {
      總_in_69 = OrderSelect(子_in_6,SELECT_BY_POS,MODE_TRADES) ;
      if ( OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
      
      if ( OrderType() == 1 )
       {
       子_in_4 = OrderClose(OrderTicket(),OrderLots(),MarketInfo(OrderSymbol(),10),5,Red) ;
       }
      if ( OrderType() == 5 )
       {
       總_in_69 = OrderDelete(OrderTicket(),0xFFFFFFFF) ;
       }
      if ( 子_in_4 <= 0 )   continue;
      PlaySound("ok.wav"); 
      }
   }}}}
 if ( 木_0 != 1 )   return;
 臨_st_7 = "buy";
 臨_in_8 = 0;
 for (臨_in_9 = OrdersTotal() - 1 ; 臨_in_9 >= 0 ; 臨_in_9 = 臨_in_9 - 1)
  {
  總_in_69 = OrderSelect(臨_in_9,SELECT_BY_POS,MODE_TRADES) ;
  if ( OrderSymbol() != Symbol() || OrderMagicNumber() != Magic || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
  
  if ( 臨_st_7 == "buy" && OrderType() == 0 )
   {
   臨_in_8 = 臨_in_8 + 1;
   }
  if ( 臨_st_7 == "sell" && OrderType() == 1 )
   {
   臨_in_8 = 臨_in_8 + 1;
   }
  if ( 臨_st_7 == "buystop" && OrderType() == 4 )
   {
   臨_in_8 = 臨_in_8 + 1;
   }
  if ( 臨_st_7 != "sellstop" || OrderType() != 5 )   continue;
  臨_in_8 = 臨_in_8 + 1;
  }
 臨_in_10 = 臨_in_8;
 臨_st_11 = "sell";
 臨_in_12 = 0;
 for (臨_in_13 = OrdersTotal() - 1 ; 臨_in_13 >= 0 ; 臨_in_13 = 臨_in_13 - 1)
  {
  總_in_69 = OrderSelect(臨_in_13,SELECT_BY_POS,MODE_TRADES) ;
  if ( OrderSymbol() != Symbol() || OrderMagicNumber() != Magic || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
  
  if ( 臨_st_11 == "buy" && OrderType() == 0 )
   {
   臨_in_12 = 臨_in_12 + 1;
   }
  if ( 臨_st_11 == "sell" && OrderType() == 1 )
   {
   臨_in_12 = 臨_in_12 + 1;
   }
  if ( 臨_st_11 == "buystop" && OrderType() == 4 )
   {
   臨_in_12 = 臨_in_12 + 1;
   }
  if ( 臨_st_11 != "sellstop" || OrderType() != 5 )   continue;
  臨_in_12 = 臨_in_12 + 1;
  }
 if ( 臨_in_10 + 臨_in_12 <= 0 )   return;
 子_in_7 = 0 ;
 if ( 木_3 != "Button5" || 總_bo_34 != 1 )   return;
 子_in_8 = MessageBox("點擊確定(Y)表示將全部平倉!是否繼續?","友情提醒：",52) ;
 if ( 子_in_8 != 6 )   return;
 臨_st_14 = "Ticket";
 臨_st_15 = "sell";
 臨_in_16 = 0;
 臨_do_17 = 0.0;
 for (臨_in_18 = OrdersTotal() - 1 ; 臨_in_18 >= 0 ; 臨_in_18 = 臨_in_18 - 1)
  {
  if ( !(OrderSelect(臨_in_18,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
  
  if ( 臨_st_15 == "buy" && OrderType() == 0 && OrderTicket() > 臨_in_16 )
   {
   OrderOpenTime(); 
   OrderOpenPrice(); 
   臨_do_17 = OrderLots();
   臨_in_16 = OrderTicket();
   }
  if ( 臨_st_15 != "sell" || OrderType() != 1 || OrderTicket() <= 臨_in_16 )   continue;
  OrderOpenTime(); 
  OrderOpenPrice(); 
  臨_do_17 = OrderLots();
  臨_in_16 = OrderTicket();
  }
 if ( 臨_st_14 == "Ticket" )
  {
  臨_do_19 = 臨_in_16;
  }
 else
  {
  if ( 臨_st_14 == "Lots" )
   {
   臨_do_19 = 臨_do_17;
   }
  else
   {
   臨_do_19 = 0.0;
  }}
 臨_in_20 = 臨_do_19;
 臨_st_21 = "Ticket";
 臨_st_22 = "buy";
 臨_in_23 = 0;
 臨_do_24 = 0.0;
 for (臨_in_25 = OrdersTotal() - 1 ; 臨_in_25 >= 0 ; 臨_in_25 = 臨_in_25 - 1)
  {
  if ( !(OrderSelect(臨_in_25,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
  
  if ( 臨_st_22 == "buy" && OrderType() == 0 && OrderTicket() > 臨_in_23 )
   {
   OrderOpenTime(); 
   OrderOpenPrice(); 
   臨_do_24 = OrderLots();
   臨_in_23 = OrderTicket();
   }
  if ( 臨_st_22 != "sell" || OrderType() != 1 || OrderTicket() <= 臨_in_23 )   continue;
  OrderOpenTime(); 
  OrderOpenPrice(); 
  臨_do_24 = OrderLots();
  臨_in_23 = OrderTicket();
  }
 if ( 臨_st_21 == "Ticket" )
  {
  臨_do_26 = 臨_in_23;
  }
 else
  {
  if ( 臨_st_21 == "Lots" )
   {
   臨_do_26 = 臨_do_24;
   }
  else
   {
   臨_do_26 = 0.0;
  }}
  if(OrderCloseBy(臨_do_26,臨_in_20,0xFFFFFFFF)){
 do
  {
  臨_st_27 = "Ticket";
  臨_st_28 = "sell";
  臨_in_29 = 0;
  臨_do_30 = 0.0;
  for (臨_in_31 = OrdersTotal() - 1 ; 臨_in_31 >= 0 ; 臨_in_31 = 臨_in_31 - 1)
   {
   if ( !(OrderSelect(臨_in_31,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
   
   if ( 臨_st_28 == "buy" && OrderType() == 0 && OrderTicket() > 臨_in_29 )
    {
    OrderOpenTime(); 
    OrderOpenPrice(); 
    臨_do_30 = OrderLots();
    臨_in_29 = OrderTicket();
    }
   if ( 臨_st_28 != "sell" || OrderType() != 1 || OrderTicket() <= 臨_in_29 )   continue;
   OrderOpenTime(); 
   OrderOpenPrice(); 
   臨_do_30 = OrderLots();
   臨_in_29 = OrderTicket();
   }
  if ( 臨_st_27 == "Ticket" )
   {
   臨_do_32 = 臨_in_29;
   }
  else
   {
   if ( 臨_st_27 == "Lots" )
    {
    臨_do_32 = 臨_do_30;
    }
   else
    {
    臨_do_32 = 0.0;
   }}
  臨_in_33 = 臨_do_32;
  臨_st_34 = "Ticket";
  臨_st_35 = "buy";
  臨_in_36 = 0;
  臨_do_37 = 0.0;
  for (臨_in_38 = OrdersTotal() - 1 ; 臨_in_38 >= 0 ; 臨_in_38 = 臨_in_38 - 1)
   {
   if ( !(OrderSelect(臨_in_38,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
   
   if ( 臨_st_35 == "buy" && OrderType() == 0 && OrderTicket() > 臨_in_36 )
    {
    OrderOpenTime(); 
    OrderOpenPrice(); 
    臨_do_37 = OrderLots();
    臨_in_36 = OrderTicket();
    }
   if ( 臨_st_35 != "sell" || OrderType() != 1 || OrderTicket() <= 臨_in_36 )   continue;
   OrderOpenTime(); 
   OrderOpenPrice(); 
   臨_do_37 = OrderLots();
   臨_in_36 = OrderTicket();
   }
  if ( 臨_st_34 == "Ticket" )
   {
   臨_do_39 = 臨_in_36;
   }
  else
   {
   if ( 臨_st_34 == "Lots" )
    {
    臨_do_39 = 臨_do_37;
    }
   else
    {
    臨_do_39 = 0.0;
   }}
  }
  while(OrderCloseBy(臨_do_39,臨_in_33,0xFFFFFFFF));
  }
 for (子_in_9 = OrdersTotal() - 1 ; 子_in_9 >= 0 ; 子_in_9 = 子_in_9 - 1)
  {
  總_in_69 = OrderSelect(子_in_9,SELECT_BY_POS,MODE_TRADES) ;
  if ( OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
  
  if ( OrderType() == 0 )
   {
   子_in_7 = OrderClose(OrderTicket(),OrderLots(),MarketInfo(OrderSymbol(),9),5,Red) ;
   }
  if ( OrderType() == 1 )
   {
   子_in_7 = OrderClose(OrderTicket(),OrderLots(),MarketInfo(OrderSymbol(),10),5,Red) ;
   }
  if ( ( OrderType() == 4 || OrderType() == 5 ) )
   {
   總_in_69 = OrderDelete(OrderTicket(),0xFFFFFFFF) ;
   }
  if ( 子_in_7 <= 0 )   continue;
  PlaySound("ok.wav"); 
  }
 }
//OnChartEvent
//---------------------  ----------------------------------------

 int deinit ()
 {

//----------------------------

 ObjectDelete("HLINE_LONGII"); 
 ObjectDelete("HLINE_SHORTII"); 
 ObjectDelete("HLINE_LONG"); 
 ObjectDelete("HLINE_SHORT"); 
 ObjectsDeleteAll(0,-1); 
 return(0); 
 }
//deinit
//---------------------  ----------------------------------------

 int lizong_7 (int 木_0)
 {
 int         子_in_1;
 int         子_in_2;
 int         子_in_3;
 int         子_in_4;
 bool        子_bo_5;
 int         子_in_6;

//----------------------------

 子_in_3 = 0 ;
 子_in_4 = 0 ;
 子_bo_5 = true ;
 for ( ; ; ) 
  {
  for (子_in_6 = OrdersTotal() - 1 ; 子_in_6 >= 0 ; 子_in_6 = 子_in_6 - 1)
   {
   if ( !(OrderSelect(子_in_6,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
   子_in_3 = OrderType() ;
   if ( 子_in_3 == 0 && ( 木_0 == 1 || 木_0 == 0 ) )
    {
    子_bo_5 = OrderClose(OrderTicket(),OrderLots(),NormalizeDouble(Bid,Digits()),總_in_22,Blue) ;
    if ( 子_bo_5 )
     {
     Comment("",OrderTicket(),"",OrderProfit(),"     ",TimeToString(TimeCurrent(),TIME_SECONDS)); 
    }}
   if ( 子_in_3 == 1 && ( 木_0 == -1 || 木_0 == 0 ) )
    {
    子_bo_5 = OrderClose(OrderTicket(),OrderLots(),NormalizeDouble(Ask,Digits()),總_in_22,Red) ;
    if ( 子_bo_5 )
     {
     Comment("",OrderTicket(),"",OrderProfit(),"     ",TimeToString(TimeCurrent(),TIME_SECONDS)); 
    }}
   if ( 子_in_3 == 4 && ( 木_0 == 1 || 木_0 == 0 ) )
    {
    子_bo_5 = OrderDelete(OrderTicket(),0xFFFFFFFF) ;
    }
   if ( 子_in_3 == 5 && ( 木_0 == -1 || 木_0 == 0 ) )
    {
    子_bo_5 = OrderDelete(OrderTicket(),0xFFFFFFFF) ;
    }
   if ( 子_bo_5 )   continue;
   子_in_1 = GetLastError() ;
   if ( 子_in_1 < 2 )   continue;
   
   if ( 子_in_1 == 129 )
    {
    Comment("",TimeToString(TimeCurrent(),TIME_SECONDS)); 
    RefreshRates(); 
     continue;
    }
   if ( 子_in_1 == 146 )
    {
    if ( !(IsTradeContextBusy()) )   continue;
    Sleep(2000); 
     continue;
    }
   Comment("",子_in_1,"",OrderTicket(),"     ",TimeToString(TimeCurrent(),TIME_SECONDS)); 
   }
  子_in_4 = 0 ;
  for (子_in_6 = 0 ; 子_in_6 < OrdersTotal() ; 子_in_6 = 子_in_6 + 1)
   {
   if ( !(OrderSelect(子_in_6,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || OrderMagicNumber() != Magic )   continue;
   子_in_3 = OrderType() ;
   if ( ( 子_in_3 == 4 || 子_in_3 == 0 ) && ( 木_0 == 1 || 木_0 == 0 ) )
    {
    子_in_4 = 子_in_4 + 1;
    }
   if ( ( 子_in_3  !=  5 && 子_in_3 != 1 ) || ( 木_0  !=  -1 && 木_0 != 0 ) )   continue;
   子_in_4 = 子_in_4 + 1;
   }
  if ( 子_in_4 == 0 )   break;
  子_in_2 = 子_in_2 + 1;
  if ( 子_in_2 > 10 )
   {
   Alert(Symbol(),"平倉超過10次",子_in_4); 
   return(0); 
   }
  Sleep(1000); 
  RefreshRates(); 
   continue;
  }
 return(1); 
 }
//lizong_7
//---------------------  ----------------------------------------

 int lizong_8 (int 木_0)
 {

//----------------------------

 if ( 木_0 > 43200 )
  {
  return(0); 
  }
 if ( 木_0 > 10080 )
  {
  return(43200); 
  }
 if ( 木_0 > 1440 )
  {
  return(10080); 
  }
 if ( 木_0 > 240 )
  {
  return(1440); 
  }
 if ( 木_0 > 60 )
  {
  return(240); 
  }
 if ( 木_0 > 30 )
  {
  return(60); 
  }
 if ( 木_0 > 15 )
  {
  return(30); 
  }
 if ( 木_0 > 5 )
  {
  return(15); 
  }
 if ( 木_0 > 1 )
  {
  return(5); 
  }
 if ( 木_0 == 1 )
  {
  return(1); 
  }
 if ( 木_0 == 0 )
  {
  return(Period()); 
  }
 return(0); 
 }
//lizong_8
//---------------------  ----------------------------------------

 void lizong_9 (int 木_0,int 木_1,int 木_2,int 木_3)
 {

//----------------------------
 int        臨_in_1;
 int        臨_in_2;
 int        臨_in_3;
 double     臨_do_4;
 int        臨_in_5;

 while (木_2 > 0)
  {
  臨_in_1 = 木_1;
  臨_in_2 = 木_0;
  臨_in_3 = -1;
  臨_do_4 = 0.0;
  for (臨_in_5 = OrdersTotal() - 1 ; 臨_in_5 >= 0 ; 臨_in_5 = 臨_in_5 - 1)
   {
   if ( !(OrderSelect(臨_in_5,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || ( OrderMagicNumber()  !=  臨_in_1 && 臨_in_1 != -1 ) || ( OrderType()  !=  臨_in_2 && 臨_in_2 != -100 ) )   continue;
   
   if ( 木_3 == 1 && 臨_do_4<OrderProfit() )
    {
    臨_do_4 = OrderProfit();
    臨_in_3 = OrderTicket();
    }
   if ( 木_3 != 2 || ( !(臨_do_4>OrderProfit()) && !(臨_do_4==0.0) ) )   continue;
   臨_do_4 = OrderProfit();
   臨_in_3 = OrderTicket();
   }
  if ( OrderSelect(臨_in_3,SELECT_BY_TICKET,MODE_TRADES) )
   {
   if ( 木_3 == 1 && OrderProfit()>=0.0 && OrderClose(OrderTicket(),OrderLots(),OrderClosePrice(),0,0xFFFFFFFF) )
    {
    木_2 = 木_2 - 1;
    }
   if ( 木_3 == 1 && OrderProfit()<0.0 )
    {
    木_2 = 木_2 - 1;
    }
   if ( 木_3 == 2 && OrderProfit()<0.0 && OrderClose(OrderTicket(),OrderLots(),OrderClosePrice(),0,0xFFFFFFFF) )
    {
    木_2 = 木_2 - 1;
    }
   if ( 木_3 == 2 && OrderProfit()>=0.0 )
    {
    木_2 = 木_2 - 1;
   }}
  else
   {
   木_2 = 木_2 - 1;
   }
  }
 }
//lizong_9
//---------------------  ----------------------------------------

 double lizong_10 (int 木_0,int 木_1,int 木_2,int 木_3)
 {
 double      子_x[100];
 int         子_in_1;
 int         子_in_2;
 double      子_do_3;

//----------------------------

 子_in_2 = 0 ;
 子_do_3 = 0.0 ;
 ArrayInitialize(子_x,0.0); 
 子_in_1 = 0 ;
 for (子_in_2 = OrdersTotal() - 1 ; 子_in_2 >= 0 ; 子_in_2 = 子_in_2 - 1)
  {
  if ( !(OrderSelect(子_in_2,SELECT_BY_POS,MODE_TRADES)) || OrderSymbol() != Symbol() || ( OrderMagicNumber()  !=  木_1 && 木_1 != -1 ) || ( OrderType()  !=  木_0 && 木_0 != -100 ) )   continue;
  
  if ( 木_2 == 1 && OrderProfit()>=0.0 )
   {
   子_x[子_in_1] = OrderProfit();
   子_in_1 = 子_in_1 + 1;
   }
  if ( 木_2 != 2 || !(OrderProfit()<0.0) )   continue;
  子_x[子_in_1] =  -(OrderProfit());
  子_in_1 = 子_in_1 + 1;
  }
 ArraySort(子_x,0,0,2); 
 子_do_3 = 0.0 ;
 for (子_in_2 = 0 ; 子_in_2 < 木_3 ; 子_in_2 = 子_in_2 + 1)
  {
  子_do_3 = 子_do_3 + 子_x[子_in_2] ;
  }
 return(子_do_3); 
 }
//lizong_10
//---------------------  ----------------------------------------
