---
UID: NF:commctrl.ListView_RemoveGroup
title: ListView_RemoveGroup macro
author: windows-driver-content
description: Removes a group from a list-view control. You can use this macro or send the LVM_REMOVEGROUP message explicitly.
old-location: controls\ListView_RemoveGroup.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_removegroup.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ListView_RemoveGroup, ListView_RemoveGroup macro [Windows Controls], _win32_ListView_RemoveGroup, _win32_ListView_RemoveGroup_cpp, commctrl/ListView_RemoveGroup, controls.ListView_RemoveGroup, controls._win32_ListView_RemoveGroup
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
-	ListView_RemoveGroup
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_RemoveGroup macro


## -description


Removes a group from a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/c6f4f54c-4cf8-47d0-8e96-fa8a1df0501b">LVM_REMOVEGROUP</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param iGroupId

Type: <b>int</b>


## -remarks



To use <b>ListView_RemoveGroup</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



