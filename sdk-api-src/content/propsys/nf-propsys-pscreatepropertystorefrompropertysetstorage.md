---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PSCreatePropertyStoreFromPropertySetStorage function


## -description


Wraps an <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a> interface in an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> interface.


## -parameters




### -param ppss [in]

Type: <b><a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a> interface.


### -param grfMode [in]

Type: <b>DWORD</b>

Specifies the access mode to enforce. grfMode should match the access mode used to open the <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>. Valid values are as follows:



#### STGM_READ

Calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536963">IPropertyStore::SetValue</a>update an internal cache of properties, and calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536957">IPropertyStore::Commit</a>call the appropriate <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a> methods to write out the changed properties.



#### STGM_WRITE

Not supported.



#### STGM_READWRITE

Not supported.


### -param riid [in]

Type: <b>REFIID</b>

Reference to an IID.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer specified in <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function wraps an <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a> interface in an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> interface. Any value other than <b>STGM_READ</b> for <i>grfMode</i>, causes calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536963">IPropertyStore::SetValue</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff536957">IPropertyStore::Commit</a> to fail with <b>STG_E_ACCESSDENIED.</b>



