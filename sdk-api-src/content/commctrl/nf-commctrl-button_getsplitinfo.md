---
UID: NF:commctrl.Button_GetSplitInfo
title: Button_GetSplitInfo macro
author: windows-sdk-content
description: Gets information for a specified split button control. Use this macro or send the BCM_GETSPLITINFO message explicitly.
old-location: controls\Button_GetSplitInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_getsplitinfo.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: Button_GetSplitInfo, Button_GetSplitInfo macro [Windows Controls], _shell_Button_GetSplitInfo, _shell_Button_GetSplitInfo_cpp, commctrl/Button_GetSplitInfo, controls.Button_GetSplitInfo, controls._shell_Button_GetSplitInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Button_GetSplitInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Button_GetSplitInfo macro


## -description


Gets information for a specified split button control. Use this macro or send the <a href="https://msdn.microsoft.com/d608440d-b8d8-4e32-9128-08b7566b185c">BCM_GETSPLITINFO</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control.


### -param pInfo [in, out]

Type: <b><a href="https://msdn.microsoft.com/ea2292c3-1dad-4e4f-9ebc-1719c86848c6">BUTTON_SPLITINFO</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/ea2292c3-1dad-4e4f-9ebc-1719c86848c6">BUTTON_SPLITINFO</a> structure to receive information on the button specified by <i>hwnd</i>. The calling application is responsible for allocating the memory for the structure. Set the <b>mask</b> member of this structure to determine what information to receive.


## -remarks



Use this macro only with the <a href="Button_Styles.htm">BS_SPLITBUTTON</a> and <a href="Button_Styles.htm">BS_DEFSPLITBUTTON</a> button styles.




## -see-also




<a href="https://msdn.microsoft.com/30254cb5-43cd-407f-8ad6-bd7f9ec3edc7">Button Styles</a>



<a href="https://msdn.microsoft.com/bfc8b88b-0da2-46f6-b8c2-72f693ee1e7b">Button Types</a>



<b>Conceptual</b>



<b>Reference</b>
 

 

