---
UID: NN:propsys.IPropertyChangeArray
title: IPropertyChangeArray (propsys.h)
description: Exposes methods for several multiple change operations that may be passed to IFileOperation.
helpviewer_keywords: ["IPropertyChangeArray","IPropertyChangeArray interface [Windows Properties]","IPropertyChangeArray interface [Windows Properties]","described","_shell_IPropertyChangeArray","properties.IPropertyChangeArray","propsys/IPropertyChangeArray","shell.IPropertyChangeArray"]
old-location: properties\IPropertyChangeArray.htm
tech.root: properties
ms.assetid: c7de40d0-9fe6-4c4b-ba17-c4648501ce0a
ms.date: 12/05/2018
ms.keywords: IPropertyChangeArray, IPropertyChangeArray interface [Windows Properties], IPropertyChangeArray interface [Windows Properties],described, _shell_IPropertyChangeArray, properties.IPropertyChangeArray, propsys/IPropertyChangeArray, shell.IPropertyChangeArray
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyChangeArray
 - propsys/IPropertyChangeArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyChangeArray
---

# IPropertyChangeArray interface


## -description

Exposes methods for several multiple change operations that may be passed to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>.

## -inheritance

The <b>IPropertyChangeArray</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertyChangeArray</b> also has these types of members:

## -remarks

Either call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with a class identifier (CLSID) of <b>CLSID_PropertyChangeArray</b> or call <a href="/windows/desktop/api/propsys/nf-propsys-pscreatepropertychangearray">PSCreatePropertyChangeArray</a> to obtain a standard implementation of this interface. This is a container interface that allows multiple changes to be passed to a single file operation to prevent accessing a file multiple times.
