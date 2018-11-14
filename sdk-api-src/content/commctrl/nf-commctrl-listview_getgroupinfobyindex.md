---
UID: NF:commctrl.ListView_GetGroupInfoByIndex
title: ListView_GetGroupInfoByIndex macro
author: windows-sdk-content
description: Gets information on a specified group. Use this macro or send the LVM_GETGROUPINFOBYINDEX message explicitly.
old-location: controls\ListView_GetGroupInfoByIndex.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getgroupinfobyindex.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ListView_GetGroupInfoByIndex, ListView_GetGroupInfoByIndex macro [Windows Controls], _shell_ListView_GetGroupInfoByIndex, _shell_ListView_GetGroupInfoByIndex_cpp, commctrl/ListView_GetGroupInfoByIndex, controls.ListView_GetGroupInfoByIndex, controls._shell_ListView_GetGroupInfoByIndex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - ListView_GetGroupInfoByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- ListView_GetGroupInfoByIndex
: 
---

# ListView_GetGroupInfoByIndex macro


## -description


Gets information on a specified group. Use this macro or send the <a href="https://msdn.microsoft.com/c40cb2c5-47c4-46ca-84fa-c017a9b1be15">LVM_GETGROUPINFOBYINDEX</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control.


### -param iIndex [in]

Type: <b>int</b>

The index of the group.


### -param pgrp [in, out]

Type: <b>PLVGROUP</b>

A pointer to an <a href="https://msdn.microsoft.com/512a8524-d5f9-47c0-a28e-47c3c1a713bf">LVGROUP</a> structure to receive information on the group specified by <i>iIndex</i>. The calling application is responsible for allocating memory for the structure and any buffers in the structure, such as, the one pointed to by <b>pszHeader</b>. Set any contingent members of the structure, such as, <b>cchHeader</b>—the size of the buffer pointed to by <b>pszHeader</b> in <b>WCHAR</b><b>s</b>, including the terminating <b>NULL</b>. Set <b>cbSize</b> to the size of <b>LVGROUP</b> in bytes.

The message receiver is responsible for setting the structure members with information for the group specified by <i>iIndex</i>.

