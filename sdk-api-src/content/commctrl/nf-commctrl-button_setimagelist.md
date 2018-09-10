---
UID: NF:commctrl.Button_SetImageList
title: Button_SetImageList macro
author: windows-sdk-content
description: Assigns an image list to a button control. You can use this macro or send the BCM_SETIMAGELIST message explicitly.
old-location: controls\Button_SetImageList.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_setimagelist.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Button_SetImageList, Button_SetImageList macro [Windows Controls], _win32_Button_SetImageList, _win32_Button_SetImageList_cpp, commctrl/Button_SetImageList, controls.Button_SetImageList, controls._win32_Button_SetImageList
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
 - Button_SetImageList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Button_SetImageList macro


## -description


Assigns an image list to a button control. You can use this macro or send the <a href="https://msdn.microsoft.com/805d2d9b-3e8f-4323-abaf-0dd5765cd740">BCM_SETIMAGELIST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control. 


### -param pbuttonImagelist

Type: <b>PBUTTON_IMAGELIST</b>

A pointer to a <a href="https://msdn.microsoft.com/c3a790ee-e247-47c1-9578-2b351cf725cd">BUTTON_IMAGELIST</a> structure that contains the image list information to set. 


## -remarks



<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comclt32.dll version 6.0. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>.</div>
<div> </div>


