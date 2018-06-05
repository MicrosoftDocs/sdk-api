---
UID: NF:commctrl.ListView_IsItemVisible
title: ListView_IsItemVisible macro
author: windows-sdk-content
description: Indicates whether an item in the list-view control is visible. Use this macro or send the LVM_ISITEMVISIBLE message explicitly.
old-location: controls\ListView_IsItemVisible.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_isitemvisible.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ListView_IsItemVisible, ListView_IsItemVisible macro [Windows Controls], _shell_ListView_IsItemVisible, _shell_ListView_IsItemVisible_cpp, commctrl/ListView_IsItemVisible, controls.ListView_IsItemVisible, controls._shell_ListView_IsItemVisible
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	ListView_IsItemVisible
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_IsItemVisible macro


## -description


Indicates whether an item in the list-view control is visible. Use this macro or send the <a href="https://msdn.microsoft.com/355be527-e2b9-46be-96a0-951d72216d92">LVM_ISITEMVISIBLE</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control.


### -param index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of item in list-view control.

