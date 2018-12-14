---
UID: NF:commctrl.ListView_GetCountPerPage
title: ListView_GetCountPerPage macro
author: windows-sdk-content
description: Calculates the number of items that can fit vertically in the visible area of a list-view control when in list or report view. Only fully visible items are counted. You can use this macro or send the LVM_GETCOUNTPERPAGE message explicitly.
old-location: controls\ListView_GetCountPerPage.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getcountperpage.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ListView_GetCountPerPage, ListView_GetCountPerPage macro [Windows Controls], _win32_ListView_GetCountPerPage, _win32_ListView_GetCountPerPage_cpp, commctrl/ListView_GetCountPerPage, controls.ListView_GetCountPerPage, controls._win32_ListView_GetCountPerPage
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
 - ListView_GetCountPerPage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetCountPerPage macro


## -description


Calculates the number of items that can fit vertically in the visible area of a list-view control when in list or report view. Only fully visible items are counted. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774917(v=VS.85).aspx">LVM_GETCOUNTPERPAGE</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 

