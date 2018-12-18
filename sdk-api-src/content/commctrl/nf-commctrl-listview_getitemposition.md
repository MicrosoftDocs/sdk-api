---
UID: NF:commctrl.ListView_GetItemPosition
title: ListView_GetItemPosition macro
author: windows-sdk-content
description: Gets the position of a list-view item. You can use this macro or explicitly send the LVM_GETITEMPOSITION message.
old-location: controls\ListView_GetItemPosition.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getitemposition.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ListView_GetItemPosition, ListView_GetItemPosition macro [Windows Controls], _win32_ListView_GetItemPosition, _win32_ListView_GetItemPosition_cpp, commctrl/ListView_GetItemPosition, controls.ListView_GetItemPosition, controls._win32_ListView_GetItemPosition
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
 - ListView_GetItemPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetItemPosition macro


## -description


Gets the position of a list-view item. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/en-us/library/Bb761048(v=VS.85).aspx">LVM_GETITEMPOSITION</a> message. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param i

Type: <b>int</b>

The index of the list-view item. 


### -param ppt

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that receives the position of the item's upper-left corner, in view coordinates. 

