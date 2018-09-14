---
UID: NF:commctrl.ListView_GetBkImage
title: ListView_GetBkImage macro
author: windows-sdk-content
description: Gets the background image in a list-view control. You can use this macro or send the LVM_GETBKIMAGE message explicitly.
old-location: controls\ListView_GetBkImage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getbkimage.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ListView_GetBkImage, ListView_GetBkImage macro [Windows Controls], _win32_ListView_GetBkImage, _win32_ListView_GetBkImage_cpp, commctrl/ListView_GetBkImage, controls.ListView_GetBkImage, controls._win32_ListView_GetBkImage
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
 - ListView_GetBkImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetBkImage macro


## -description


Gets the background image in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774907(v=VS.85).aspx">LVM_GETBKIMAGE</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the list-view control. 


### -param plvbki

Type: <b>LPLVBKIMAGE</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb774742(v=VS.85).aspx">LVBKIMAGE</a> structure that will receive the background image information. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775065(v=VS.85).aspx">ListView_SetBkImage</a>
 

 

