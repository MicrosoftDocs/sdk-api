---
UID: NF:commctrl.ListView_GetItemSpacing
title: ListView_GetItemSpacing macro
author: windows-sdk-content
description: Determines the spacing between items in a list-view control. You can use this macro or send the LVM_GETITEMSPACING message explicitly.
old-location: controls\ListView_GetItemSpacing.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getitemspacing.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ListView_GetItemSpacing, ListView_GetItemSpacing macro [Windows Controls], _win32_ListView_GetItemSpacing, _win32_ListView_GetItemSpacing_cpp, commctrl/ListView_GetItemSpacing, controls.ListView_GetItemSpacing, controls._win32_ListView_GetItemSpacing
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
 - ListView_GetItemSpacing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetItemSpacing macro


## -description


Determines the spacing between items in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761051(v=VS.85).aspx">LVM_GETITEMSPACING</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param fSmall

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

A view for which to retrieve the item spacing. This parameter is <b>TRUE</b> for small icon view, or <b>FALSE</b> for icon view. 

