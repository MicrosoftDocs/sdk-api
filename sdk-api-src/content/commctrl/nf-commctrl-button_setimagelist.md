---
UID: NF:commctrl.Button_SetImageList
title: Button_SetImageList macro
author: windows-sdk-content
description: Assigns an image list to a button control. You can use this macro or send the BCM_SETIMAGELIST message explicitly.
old-location: controls\Button_SetImageList.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_setimagelist.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Button_SetImageList, Button_SetImageList macro [Windows Controls], _win32_Button_SetImageList, _win32_Button_SetImageList_cpp, commctrl/Button_SetImageList, controls.Button_SetImageList, controls._win32_Button_SetImageList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.redist: 
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
req.lib: 
req.dll: 
req.irql: 
---

# Button_SetImageList macro


## -description


Assigns an image list to a button control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775975(v=VS.85).aspx">BCM_SETIMAGELIST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control. 


### -param pbuttonImagelist

Type: <b>PBUTTON_IMAGELIST</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb775953(v=VS.85).aspx">BUTTON_IMAGELIST</a> structure that contains the image list information to set. 


## -remarks



<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comclt32.dll version 6.0. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>.</div>
<div> </div>


