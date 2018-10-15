---
UID: NF:commctrl.Button_GetImageList
title: Button_GetImageList macro
author: windows-sdk-content
description: Gets the BUTTON_IMAGELIST structure that describes the image list that is set for a button control. You can use this macro or send the BCM_GETIMAGELIST message explicitly.
old-location: controls\Button_GetImageList.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_getimagelist.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: Button_GetImageList, Button_GetImageList macro [Windows Controls], _win32_Button_GetImageList, _win32_Button_GetImageList_cpp, commctrl/Button_GetImageList, controls.Button_GetImageList, controls._win32_Button_GetImageList
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
 - Button_GetImageList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Button_GetImageList macro


## -description


Gets the <a href="https://msdn.microsoft.com/en-us/library/Bb775953(v=VS.85).aspx">BUTTON_IMAGELIST</a> structure that describes the image list that is set for a button control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775963(v=VS.85).aspx">BCM_GETIMAGELIST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the button control. 


### -param pbuttonImagelist

Type: <b>PBUTTON_IMAGELIST</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb775953(v=VS.85).aspx">BUTTON_IMAGELIST</a> structure that contains image list information. 


## -remarks



<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comclt32.dll version 6.0. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775963(v=VS.85).aspx">BCM_GETIMAGELIST</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb775953(v=VS.85).aspx">BUTTON_IMAGELIST</a>



<b>Reference</b>
 

 

