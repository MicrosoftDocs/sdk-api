---
UID: NF:commctrl.ListView_GetBkImage
title: ListView_GetBkImage macro
author: windows-sdk-content
description: Gets the background image in a list-view control. You can use this macro or send the LVM_GETBKIMAGE message explicitly.
old-location: controls\ListView_GetBkImage.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getbkimage.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ListView_GetBkImage, ListView_GetBkImage macro [Windows Controls], _win32_ListView_GetBkImage, _win32_ListView_GetBkImage_cpp, commctrl/ListView_GetBkImage, controls.ListView_GetBkImage, controls._win32_ListView_GetBkImage
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
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ListView_GetBkImage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetBkImage macro


## -description


Gets the background image in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/db0e8f31-746a-4a16-b689-68da696e3657">LVM_GETBKIMAGE</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param plvbki

Type: <b>LPLVBKIMAGE</b>

A pointer to a <a href="https://msdn.microsoft.com/d8b35356-d112-43e5-b1ad-7fb945c84e33">LVBKIMAGE</a> structure that will receive the background image information. 


#### - hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -see-also




<a href="https://msdn.microsoft.com/8ee481c7-e114-45bd-9082-16d756152e54">ListView_SetBkImage</a>
 

 

