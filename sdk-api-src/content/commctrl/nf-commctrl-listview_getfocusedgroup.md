---
UID: NF:commctrl.ListView_GetFocusedGroup
title: ListView_GetFocusedGroup macro
author: windows-driver-content
description: Gets the group that has the focus. Use this macro or send the LVM_GETFOCUSEDGROUP message explicitly.
old-location: controls\ListView_GetFocusedGroup.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getfocusedgroup.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: ListView_GetFocusedGroup, ListView_GetFocusedGroup macro [Windows Controls], _shell_ListView_GetFocusedGroup, _shell_ListView_GetFocusedGroup_cpp, commctrl/ListView_GetFocusedGroup, controls.ListView_GetFocusedGroup, controls._shell_ListView_GetFocusedGroup
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
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	ListView_GetFocusedGroup
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetFocusedGroup macro


## -description


Gets the group that has the focus. Use this macro or send the <a href="https://msdn.microsoft.com/c1902f35-84b7-4f46-89a6-e48148f06172">LVM_GETFOCUSEDGROUP</a> message explicitly. 



## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control.

