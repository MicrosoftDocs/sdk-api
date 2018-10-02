---
UID: NF:shobjidl_core.IShellItem2.GetPropertyStore
title: IShellItem2::GetPropertyStore
author: windows-sdk-content
description: Gets a property store object for specified property store flags.
old-location: shell\IShellItem2_GetPropertyStore.htm
tech.root: Shell
ms.assetid: 706b2551-a9b0-4368-babb-e54cea6d297e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetPropertyStore, GetPropertyStore method [Windows Shell], GetPropertyStore method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetPropertyStore method, IShellItem2.GetPropertyStore, IShellItem2::GetPropertyStore, _shell_IShellItem2_GetPropertyStore, shell.IShellItem2_GetPropertyStore, shobjidl_core/IShellItem2::GetPropertyStore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellItem2.GetPropertyStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellItem2::GetPropertyStore


## -description


Gets a property store object for specified property store flags.


## -parameters




### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/d3fde1b9-b19f-431d-9cea-bffc289ee683">GETPROPERTYSTOREFLAGS</a></b>

The <a href="https://msdn.microsoft.com/d3fde1b9-b19f-431d-9cea-bffc289ee683">GETPROPERTYSTOREFLAGS</a> constants that modify the property store object.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the object to be retrieved.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of an <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  When this method is called on a property store for a file, that file is held open for the lifetime of the <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a> object.</div>
<div> </div>


