---
UID: NF:commctrl.ListView_InsertGroupSorted
title: ListView_InsertGroupSorted macro (commctrl.h)
author: windows-sdk-content
description: Inserts a group into an ordered list of groups. You can use this macro or send the LVM_INSERTGROUPSORTED message explicitly.
old-location: controls\ListView_InsertGroupSorted.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_insertgroupsorted.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListView_InsertGroupSorted, ListView_InsertGroupSorted macro [Windows Controls], _win32_ListView_InsertGroupSorted, _win32_ListView_InsertGroupSorted_cpp, commctrl/ListView_InsertGroupSorted, controls.ListView_InsertGroupSorted, controls._win32_ListView_InsertGroupSorted
ms.topic: macro
f1_keywords: ["commctrl/ListView_InsertGroupSorted"]
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
 - ListView_InsertGroupSorted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_InsertGroupSorted macro


## -description


Inserts a group into an ordered list of groups. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-insertgroupsorted">LVM_INSERTGROUPSORTED</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


### -param structInsert

Type: <b>PLVINSERTGROUPSORTED</b>

<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-taglvinsertgroupsorted">LVINSERTGROUPSORTED</a>

## -remarks



To use <b>ListView_InsertGroupSorted</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>. 



