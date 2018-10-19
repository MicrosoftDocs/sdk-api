---
UID: NF:commctrl.Button_GetIdealSize
title: Button_GetIdealSize macro
author: windows-sdk-content
description: Gets the size of the button that best fits the text and image, if an image list is present. You can use this macro or send the BCM_GETIDEALSIZE message explicitly.
old-location: controls\Button_GetIdealSize.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_getidealsize.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: Button_GetIdealSize, Button_GetIdealSize macro [Windows Controls], _win32_Button_GetIdealSize, _win32_Button_GetIdealSize_cpp, commctrl/Button_GetIdealSize, controls.Button_GetIdealSize, controls._win32_Button_GetIdealSize
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Button_GetIdealSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Button_GetIdealSize macro


## -description


Gets the size of the button that best fits the text and image, if an image list is present. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775961(v=VS.85).aspx">BCM_GETIDEALSIZE</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the button control. 


### -param psize

Type: <b><a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure that receives the desired size of the button including the text and image list if present. 


## -remarks



This macro is most applicable to PushButtons. When sent to a PushButton, the macro retrieves the bounding rectangle required to display the button's text. And, if the PushButton has an image list, the bounding rectangle is also sized to include the button's image. 

When sent to a button of any other type, the size of the control's window rectangle is retrieved.

<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comclt32.dll version 6.0. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775961(v=VS.85).aspx">BCM_GETIDEALSIZE</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a>
 

 

