---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnItemStateChanged
title: INameSpaceTreeControlEvents::OnItemStateChanged
author: windows-sdk-content
description: Not implemented.
old-location: shell\INameSpaceTreeControlEvents_OnItemStateChanged.htm
old-project: shell
ms.assetid: 0154d97b-44db-40bf-a202-e97ba318555f
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnItemStateChanged method, INameSpaceTreeControlEvents.OnItemStateChanged, INameSpaceTreeControlEvents::OnItemStateChanged, OnItemStateChanged, OnItemStateChanged method [Windows Shell], OnItemStateChanged method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnItemStateChanged, shell.INameSpaceTreeControlEvents_OnItemStateChanged, shobjidl/INameSpaceTreeControlEvents::OnItemStateChanged
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl.h
req.include-header: Shobjidl.h
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl.h
api_name:
-	INameSpaceTreeControlEvents.OnItemStateChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeControlEvents::OnItemStateChanged


## -description


Not implemented.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the shell item for which the state has changed.


### -param nstcisMask [in]

Type: <b><a href="https://msdn.microsoft.com/1f3fd526-c044-41ff-9e05-c6d91d386b42">NSTCITEMSTATE</a></b>

One or more values from the <a href="https://msdn.microsoft.com/1f3fd526-c044-41ff-9e05-c6d91d386b42">NSTCITEMSTATE</a> enumeration that indicates what pieces of information the caller wants to set.


### -param nstcisState [in]

Type: <b><a href="https://msdn.microsoft.com/1f3fd526-c044-41ff-9e05-c6d91d386b42">NSTCITEMSTATE</a></b>

One or more values from the <a href="https://msdn.microsoft.com/1f3fd526-c044-41ff-9e05-c6d91d386b42">NSTCITEMSTATE</a> enumeration that indicates the values that are to be set.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



