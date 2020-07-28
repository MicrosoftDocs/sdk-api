---
UID: NF:commctrl.Button_GetIdealSize
title: Button_GetIdealSize macro (commctrl.h)
description: Gets the size of the button that best fits the text and image, if an image list is present. You can use this macro or send the BCM_GETIDEALSIZE message explicitly.
helpviewer_keywords: ["Button_GetIdealSize","Button_GetIdealSize macro [Windows Controls]","_win32_Button_GetIdealSize","_win32_Button_GetIdealSize_cpp","commctrl/Button_GetIdealSize","controls.Button_GetIdealSize","controls._win32_Button_GetIdealSize"]
old-location: controls\Button_GetIdealSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_getidealsize.htm
ms.date: 12/05/2018
ms.keywords: Button_GetIdealSize, Button_GetIdealSize macro [Windows Controls], _win32_Button_GetIdealSize, _win32_Button_GetIdealSize_cpp, commctrl/Button_GetIdealSize, controls.Button_GetIdealSize, controls._win32_Button_GetIdealSize
f1_keywords:
- commctrl/Button_GetIdealSize
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Button_GetIdealSize macro


## -description


Gets the size of the button that best fits the text and image, if an image list is present. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/bcm-getidealsize">BCM_GETIDEALSIZE</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the button control. 


### -param psize

Type: <b><a href="https://docs.microsoft.com/previous-versions/dd145106(v=vs.85)">SIZE</a>*</b>

A pointer to a <a href="https://docs.microsoft.com/previous-versions/dd145106(v=vs.85)">SIZE</a> structure that receives the desired size of the button including the text and image list if present. 


## -remarks



This macro is most applicable to PushButtons. When sent to a PushButton, the macro retrieves the bounding rectangle required to display the button's text. And, if the PushButton has an image list, the bounding rectangle is also sized to include the button's image. 

When sent to a button of any other type, the size of the control's window rectangle is retrieved.

<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comclt32.dll version 6.0. For more information on manifests, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/bcm-getidealsize">BCM_GETIDEALSIZE</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://docs.microsoft.com/previous-versions/dd145106(v=vs.85)">SIZE</a>
 

 

