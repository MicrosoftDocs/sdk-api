---
UID: NF:propsys.PSCreatePropertyStoreFromObject
title: PSCreatePropertyStoreFromObject function
author: windows-driver-content
description: Accepts the IUnknown interface of an object that supports IPropertyStore or IPropertySetStorage. If the object supports IPropertySetStorage, it is wrapped so that it supports IPropertyStore.
old-location: properties\PSCreatePropertyStoreFromObject.htm
old-project: properties
ms.assetid: 010572d5-0357-4101-803e-0a27fc60ca5e
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PSCreatePropertyStoreFromObject, PSCreatePropertyStoreFromObject function [Windows Properties], STGM_READ, STGM_READWRITE, _shell_PSCreatePropertyStoreFromObject, properties.PSCreatePropertyStoreFromObject, propsys/PSCreatePropertyStoreFromObject, shell.PSCreatePropertyStoreFromObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	PSCreatePropertyStoreFromObject
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Compute Cluster Pack Client Utilities
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
 

 

