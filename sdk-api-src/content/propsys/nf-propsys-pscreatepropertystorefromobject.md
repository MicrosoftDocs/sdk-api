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

# PSCreatePropertyStoreFromObject function


## -description


Accepts the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of an object that supports <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> or <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>. If the object supports <b>IPropertySetStorage</b>, it is wrapped so that it supports <b>IPropertyStore</b>.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to an interface that supports either <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> or <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>.


### -param grfMode [in]

Type: <b>DWORD</b>

Specifies the access mode to use. One of these values:



#### STGM_READ

Open for reading.



#### STGM_READWRITE

Open for reading and writing.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the requested IID.


### -param ppv [out]

Type: <b>void**</b>

When this function returns successfully, contains the address of a pointer to an interface guaranteed to support <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the object pointed to by <i>punk</i> already supports <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>, no wrapper is created and the <i>punk</i> is returned unaltered.




## -see-also




<a href="shell.PSCreatePropertyStoreFromPropertySetStorage">PSCreatePropertyStoreFromPropertySetStorage</a>
 

 

