# cotroller中参数问题

`touch": 254, //0xFE`
`"key": 65024, //0xFE00`
`"screencap": 16646144 //0xFE0000`

具体详见MaaFramework头文件：[MaaDef.h File Reference](https://maaxyz.github.io/MaaFramework/MaaDef_8h.html)

其中有：

`#define 	MaaAdbControllerType_Touch_Mask   0xFF`
 
`#define 	MaaAdbControllerType_Key_Mask   0xFF00`
 
`#define 	MaaAdbControllerType_Screencap_Mask   0xFF0000`
 
`#define 	MaaWin32ControllerType_Touch_Mask   0xFF`
 
`#define 	MaaWin32ControllerType_Key_Mask   0xFF00`
 
`#define 	MaaWin32ControllerType_Screencap_Mask   0xFF0000`

`MaaAdbControllerTypeEnum {
  MaaAdbControllerType_Invalid = 0 , MaaAdbControllerType_Touch_Adb = 1 , MaaAdbControllerType_Touch_MiniTouch = 2 , MaaAdbControllerType_Touch_MaaTouch = 3 ,
  MaaAdbControllerType_Touch_AutoDetect = MaaAdbControllerType_Touch_Mask - 1 , MaaAdbControllerType_Key_Adb = 1 << 8 , MaaAdbControllerType_Key_MaaTouch = 2 << 8 , MaaAdbControllerType_Key_AutoDetect = MaaAdbControllerType_Key_Mask - (1 << 8) ,
  MaaAdbControllerType_Input_Preset_Adb = MaaAdbControllerType_Touch_Adb | MaaAdbControllerType_Key_Adb , MaaAdbControllerType_Input_Preset_Minitouch = MaaAdbControllerType_Touch_MiniTouch | MaaAdbControllerType_Key_Adb , MaaAdbControllerType_Input_Preset_Maatouch , MaaAdbControllerType_Input_Preset_AutoDetect ,
  MaaAdbControllerType_Screencap_FastestWay_Compatible = 1 << 16 , MaaAdbControllerType_Screencap_RawByNetcat = 2 << 16 , MaaAdbControllerType_Screencap_RawWithGzip = 3 << 16 , MaaAdbControllerType_Screencap_Encode = 4 << 16 ,
  MaaAdbControllerType_Screencap_EncodeToFile = 5 << 16 , MaaAdbControllerType_Screencap_MinicapDirect = 6 << 16 , MaaAdbControllerType_Screencap_MinicapStream = 7 << 16 , MaaAdbControllerType_Screencap_FastestLosslessWay = MaaAdbControllerType_Screencap_Mask - (2 << 16) ,
  MaaAdbControllerType_Screencap_FastestWay = MaaAdbControllerType_Screencap_Mask - (1 << 16)
}`

~~我也不知道为什么要这样写~~