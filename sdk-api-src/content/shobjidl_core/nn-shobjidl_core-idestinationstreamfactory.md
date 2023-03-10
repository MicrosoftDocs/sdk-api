---
UID: NN:shobjidl_core.IDestinationStreamFactory
title: IDestinationStreamFactory (shobjidl_core.h)
description: Exposes a method for manually copying a stream or file before applying changes to properties.
helpviewer_keywords: ["IDestinationStreamFactory","IDestinationStreamFactory interface [Windows Shell]","IDestinationStreamFactory interface [Windows Shell]","described","shell.IDestinationStreamFactory","shell_IDestinationStreamFactory","shobjidl_core/IDestinationStreamFactory"]
old-location: shell\IDestinationStreamFactory.htm
tech.root: shell
ms.assetid: 7cedf8eb-b4ef-4889-bd7b-a734e939e872
ms.date: 12/05/2018
ms.keywords: IDestinationStreamFactory, IDestinationStreamFactory interface [Windows Shell], IDestinationStreamFactory interface [Windows Shell],described, shell.IDestinationStreamFactory, shell_IDestinationStreamFactory, shobjidl_core/IDestinationStreamFactory
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDestinationStreamFactory
 - shobjidl_core/IDestinationStreamFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IDestinationStreamFactory
---

# IDestinationStreamFactory interface


## -description

Exposes a method for manually copying a stream or file before applying changes to properties.

## -inheritance

The <b>IDestinationStreamFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDestinationStreamFactory</b> also has these types of members:

## -remarks

The default copy-on-write behavior provided by <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> causes the entire source stream to be duplicated during a write operation. This can be costly for large streams, especially when a large portion of the stream is to be changed. <b>IDestinationStreamFactory</b> provides an alternative for the property handler author, who can use it manually to ensure that property changes do not corrupt the stream in case of failure. To do this, the author marks the handler as NoTransactedMode in the handler's CoClass registry key, and queries the stream for this interface.

## -see-also

<a href="/windows/desktop/properties/building-property-handlers-property-handlers">Initializing Property Handlers</a>
