---
UID: NN:propsys.IPersistSerializedPropStorage
title: IPersistSerializedPropStorage (propsys.h)
description: Exposes methods to persist serialized property storage data for later use and to restore persisted data to a new property store instance. (IPersistSerializedPropStorage)
helpviewer_keywords: ["IPersistSerializedPropStorage","IPersistSerializedPropStorage interface [Windows Shell]","IPersistSerializedPropStorage interface [Windows Shell]","described","_shell_IPersistSerializedPropStorage","propsys/IPersistSerializedPropStorage","shell.IPersistSerializedPropStorage"]
old-location: shell\IPersistSerializedPropStorage.htm
tech.root: shell
ms.assetid: d3ce6a05-b1e5-4d99-a27e-3a97a28ed8e8
ms.date: 12/05/2018
ms.keywords: IPersistSerializedPropStorage, IPersistSerializedPropStorage interface [Windows Shell], IPersistSerializedPropStorage interface [Windows Shell],described, _shell_IPersistSerializedPropStorage, propsys/IPersistSerializedPropStorage, shell.IPersistSerializedPropStorage
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Propsys.dll (version 6.0.6001 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPersistSerializedPropStorage
 - propsys/IPersistSerializedPropStorage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.dll
api_name:
 - IPersistSerializedPropStorage
---

# IPersistSerializedPropStorage interface


## -description

Exposes methods to persist serialized property storage data for later use and to restore persisted data to a new property store instance.

## -inheritance

The <b>IPersistSerializedPropStorage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPersistSerializedPropStorage</b> also has these types of members:

## -remarks

Use the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface to read and write values from and to the property store.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
The in-memory property store, created by calling <a href="/windows/desktop/api/propsys/nf-propsys-pscreatememorypropertystore">PSCreateMemoryPropertyStore</a>, provides an implementation of this interface. Use this implementation when you want to persist or restore serialized property storage data.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
<b>IPersistSerializedPropStorage</b> is not intended for custom implementation. Use the system-provided implementation associated with the in-memory property store.
