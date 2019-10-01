---
UID: NF:commctrl.ListView_RemoveGroup
title: ListView_RemoveGroup macro (commctrl.h)
author: windows-sdk-content
description: Removes a group from a list-view control. You can use this macro or send the LVM_REMOVEGROUP message explicitly.
old-location: controls\ListView_RemoveGroup.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_removegroup.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListView_RemoveGroup, ListView_RemoveGroup macro [Windows Controls], _win32_ListView_RemoveGroup, _win32_ListView_RemoveGroup_cpp, commctrl/ListView_RemoveGroup, controls.ListView_RemoveGroup, controls._win32_ListView_RemoveGroup
ms.topic: macro
f1_keywords: 
 - "commctrl/ListView_RemoveGroup"
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
 - ListView_RemoveGroup
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_RemoveGroup macro


## -description


Removes a group from a list-view control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-removegroup">LVM_REMOVEGROUP</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


### -param iGroupId

Type: <b>int</b>


## -remarks



To use <b>ListView_RemoveGroup</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>. 



