---
UID: NF:commctrl.ListView_SetColumn
title: ListView_SetColumn macro
author: windows-driver-content
description: Sets the attributes of a list-view column. You can use this macro or send the LVM_SETCOLUMN message explicitly.
old-location: controls\ListView_SetColumn.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setcolumn.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ListView_SetColumn, ListView_SetColumn macro [Windows Controls], _win32_ListView_SetColumn, _win32_ListView_SetColumn_cpp, commctrl/ListView_SetColumn, controls.ListView_SetColumn, controls._win32_ListView_SetColumn
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	ListView_SetColumn
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_SetColumn macro


## -description


Sets the attributes of a list-view column. You can use this macro or send the <a href="https://msdn.microsoft.com/8ca1c269-fd86-4561-940d-b75f8ca2b731">LVM_SETCOLUMN</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param iCol

Type: <b>int</b>

The index of the column. 


### -param pcol

Type: <b>LPLVCOLUMN</b>

A pointer to an <a href="https://msdn.microsoft.com/6ffa287d-0284-43c9-80ff-b9c90a83e855">LVCOLUMN</a> structure that contains the new column attributes. The <b>mask</b> member specifies which column attributes to set. If the <b>mask</b> member specifies the LVCF_TEXT value, the <b>pszText</b> member is the address of a null-terminated string and the <b>cchTextMax</b> member is ignored.

