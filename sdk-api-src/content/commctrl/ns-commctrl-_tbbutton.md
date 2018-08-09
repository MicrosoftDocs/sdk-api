---
UID: NS:commctrl._TBBUTTON
title: "_TBBUTTON"
author: windows-sdk-content
description: Contains information about a button in a toolbar.
old-location: controls\TBBUTTON.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\tbbutton.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPTBBUTTON, *PTBBUTTON, LPTBBUTTON, LPTBBUTTON structure pointer [Windows Controls], PTBBUTTON, PTBBUTTON structure pointer [Windows Controls], TBBUTTON, TBBUTTON structure [Windows Controls], _TBBUTTON, _win32_TBBUTTON, _win32_TBBUTTON_cpp, commctrl/LPTBBUTTON, commctrl/PTBBUTTON, commctrl/TBBUTTON, controls.TBBUTTON, controls._win32_TBBUTTON"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TBBUTTON, *PTBBUTTON, *LPTBBUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TBBUTTON
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _TBBUTTON structure


## -description


Contains information about a button in a toolbar.


## -struct-fields




### -field iBitmap

Type: <b>int</b>

Zero-based index of the button image. Set this member to I_IMAGECALLBACK, and the toolbar will send the <a href="https://msdn.microsoft.com/en-us/library/Bb787268(v=VS.85).aspx">TBN_GETDISPINFO</a> notification code to retrieve the image index when it is needed. 


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 5.81</a>. Set this member to I_IMAGENONE to indicate that the button does not have an image. The button layout will not include any space for a bitmap, only text.

If the button is a separator, that is, if <b>fsStyle</b> is set to <a href="Toolbar_Control_and_Button_Styles.htm">BTNS_SEP</a>, <b>iBitmap</b> determines the width of the separator, in pixels. For information on selecting button images from image lists, see <a href="https://msdn.microsoft.com/en-us/library/Bb787433(v=VS.85).aspx">TB_SETIMAGELIST</a> message.


### -field idCommand

Type: <b>int</b>

Command identifier associated with the button. This identifier is used in a <a href="https://msdn.microsoft.com/en-us/library/ms647591(v=VS.85).aspx">WM_COMMAND</a> message when the button is chosen. 


### -field fsState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Button state flags. This member can be a combination of the values listed in <a href="https://msdn.microsoft.com/en-us/library/Bb760437(v=VS.85).aspx">Toolbar Button States</a>. 


### -field fsStyle

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Button style. This member can be a combination of the button style values listed in <a href="https://msdn.microsoft.com/en-us/library/Bb760439(v=VS.85).aspx">Toolbar Control and Button Styles</a>. 


### -field bReserved

 


### -field dwData

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD_PTR</a></b>

Application-defined value. 


### -field iString

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT_PTR</a></b>

Zero-based index of the button string, or a pointer to a string buffer that contains text for the button. 


#### - bReserved[6]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Reserved. 


#### - bReserved[2]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Reserved. 


## -remarks



The <b>iString</b> member can return either a string pointer or an index. You can use the <a href="https://msdn.microsoft.com/en-us/library/ms648028(v=VS.85).aspx">IS_INTRESOURCE</a> macro to determine which is returned. 



