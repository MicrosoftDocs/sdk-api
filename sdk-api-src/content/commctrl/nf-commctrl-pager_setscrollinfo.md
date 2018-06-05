---
UID: NF:commctrl.Pager_SetScrollInfo
title: Pager_SetScrollInfo macro
author: windows-sdk-content
description: Sets the scrolling parameters of the pager control, including the timeout value, the lines per timeout, and the pixels per line. You can use this macro or send the PGM_SETSETSCROLLINFO message explicitly.
old-location: controls\Pager_SetScrollInfo.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_setscrollinfo.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: Pager_SetScrollInfo, Pager_SetScrollInfo macro [Windows Controls], _win32_Pager_SetScrollInfo, _win32_Pager_SetScrollInfo_cpp, commctrl/Pager_SetScrollInfo, controls.Pager_SetScrollInfo, controls._win32_Pager_SetScrollInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	Pager_SetScrollInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Pager_SetScrollInfo macro


## -description


<p class="CCE_Message">[Intended for internal use; not recommended for use in applications. This macro may not be supported in future versions of Windows.]

Sets the scrolling parameters of the pager control, including the timeout value, the lines per timeout, and the pixels per line. You can use this macro or send the <a href="https://msdn.microsoft.com/e02450b8-f2b5-45b2-9395-d7412119849c">PGM_SETSETSCROLLINFO</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param cTimeOut

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The timeout value for the scroll, in milliseconds. 


### -param cLinesPer

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of lines to scroll per timeout. 


### -param cPixelsPerLine

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of pixels per line. 


#### - hwndPager

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the pager control. 


## -remarks



This <i>cTimeOut</i> parameter controls the rate at which the pager control generates scrolling events when the control has captured the mouse input and the left mouse button is pressed. Smaller values result in faster scrolling; larger values result in slower scrolling. The default value is one-eighth of the double-click time. For more information, see <a href="https://msdn.microsoft.com/8917bc74-d925-4f67-af5c-ab8fe6ad9607">GetDoubleClickTime</a>.

By default, with each scrolling event the pager control scrolls an amount equal to the entire width or height of the control, depending on whether the pager control has a horizontal or vertical orientation. The <i>cLinesPer</i> and <i>cPixelsPerLine</i> parameters are used to override the default scrolling amount. If nonzero values are provided, the scrolling amount is the product of the two values (<i>cLinesPer</i> * <i>cPixelsPerLine</i>). 




## -see-also




<a href="https://msdn.microsoft.com/e02450b8-f2b5-45b2-9395-d7412119849c">PGM_SETSETSCROLLINFO</a>
 

 

