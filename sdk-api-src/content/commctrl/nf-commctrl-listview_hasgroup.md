---
UID: NF:commctrl.ListView_HasGroup
title: ListView_HasGroup macro
author: windows-sdk-content
description: Determines whether the list-view control has a specified group. You can use this macro or send the LVM_HASGROUP message explicitly.
old-location: controls\ListView_HasGroup.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_hasgroup.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ListView_HasGroup, ListView_HasGroup macro [Windows Controls], _win32_ListView_HasGroup, _win32_ListView_HasGroup_cpp, commctrl/ListView_HasGroup, controls.ListView_HasGroup, controls._win32_ListView_HasGroup
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
 - ListView_HasGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_HasGroup macro


## -description


Determines whether the list-view control has a specified group. You can use this macro or send the <a href="https://msdn.microsoft.com/0b8a9208-5221-4f66-8b26-7de55afe485f">LVM_HASGROUP</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param dwGroupId

Type: <b>int</b>


## -remarks



To use <b>ListView_HasGroup</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



