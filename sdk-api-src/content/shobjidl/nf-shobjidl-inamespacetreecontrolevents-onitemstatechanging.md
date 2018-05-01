---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnItemStateChanging
title: INameSpaceTreeControlEvents::OnItemStateChanging method
author: windows-driver-content
description: Called before the state of an item changes.
old-location: shell\INameSpaceTreeControlEvents_OnItemStateChanging.htm
old-project: shell
ms.assetid: ed0f431a-f3e2-4a95-a16e-6e38568dd91f
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: INameSpaceTreeControlEvents, INameSpaceTreeControlEvents interface [Windows Shell], OnItemStateChanging method, INameSpaceTreeControlEvents::OnItemStateChanging, OnItemStateChanging method [Windows Shell], OnItemStateChanging method [Windows Shell], INameSpaceTreeControlEvents interface, OnItemStateChanging,INameSpaceTreeControlEvents.OnItemStateChanging, _shell_INameSpaceTreeControlEvents_OnItemStateChanging, shell.INameSpaceTreeControlEvents_OnItemStateChanging, shobjidl/INameSpaceTreeControlEvents::OnItemStateChanging
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shobjidl.h
api_name:
-	INameSpaceTreeControlEvents.OnItemStateChanging
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeControlEvents::OnItemStateChanging method


## -description


Called before the state of an item changes.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the Shell item for which the state is going to change.


### -param nstcisMask [in]

Type: <b><a href="https://msdn.microsoft.com/1f3fd526-c044-41ff-9e05-c6d91d386b42">NSTCITEMSTATE</a></b>

One or more values from the <a href="https://msdn.microsoft.com/1f3fd526-c044-41ff-9e05-c6d91d386b42">NSTCITEMSTATE</a> enumeration that indicate which pieces of information the calling application wants to set.


### -param nstcisState [in]

Type: <b><a href="https://msdn.microsoft.com/1f3fd526-c044-41ff-9e05-c6d91d386b42">NSTCITEMSTATE</a></b>

One or more values from the <a href="https://msdn.microsoft.com/1f3fd526-c044-41ff-9e05-c6d91d386b42">NSTCITEMSTATE</a> enumeration that indicate the values that are to be set.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



