---
UID: NF:commctrl.ListView_DeleteColumn
title: ListView_DeleteColumn macro (commctrl.h)
author: windows-sdk-content
description: Removes a column from a list-view control. You can use this macro or send the LVM_DELETECOLUMN message explicitly.
old-location: controls\ListView_DeleteColumn.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_deletecolumn.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListView_DeleteColumn, ListView_DeleteColumn macro [Windows Controls], _win32_ListView_DeleteColumn, _win32_ListView_DeleteColumn_cpp, commctrl/ListView_DeleteColumn, controls.ListView_DeleteColumn, controls._win32_ListView_DeleteColumn
ms.topic: macro
f1_keywords: ["commctrl/ListView_DeleteColumn"]
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
 - ListView_DeleteColumn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_DeleteColumn macro


## -description


Removes a column from a list-view control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-deletecolumn">LVM_DELETECOLUMN</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


### -param iCol

Type: <b>int</b>

An index of the column to delete. 


## -remarks



Deleting column zero of a list-view control is supported only in ComCtl32.dll version 6 and later. Version 5 also supports deleting column zero, but only  after you use <a href="https://docs.microsoft.com/windows/desktop/Controls/ccm-setversion">CCM_SETVERSION</a> to set the version to 5 or later. In versions prior to version 5, if you must delete column zero, insert a zero length dummy column zero and delete column one and above. 



