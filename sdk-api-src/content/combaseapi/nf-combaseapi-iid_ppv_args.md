---
UID: NF:combaseapi.IID_PPV_ARGS
title: IID_PPV_ARGS macro (combaseapi.h)
description: Used to retrieve an interface pointer, supplying the IID value of the requested interface automatically based on the type of the interface pointer used. This avoids a common coding error by checking the type of the value passed at compile time.
helpviewer_keywords: ["IID_PPV_ARGS","IID_PPV_ARGS macro [Windows Shell]","IID_PPV_ARGS_Helper","_shell_IID_PPV_ARGS","combaseapi/IID_PPV_ARGS","shell.IID_PPV_ARGS"]
old-location: shell\IID_PPV_ARGS.htm
tech.root: shell
ms.assetid: 268B59FA-44EB-4777-8162-C50981CBDD09
ms.date: 07/01/2025
ms.keywords: IID_PPV_ARGS, IID_PPV_ARGS macro [Windows Shell], IID_PPV_ARGS_Helper, _shell_IID_PPV_ARGS, combaseapi/IID_PPV_ARGS, shell.IID_PPV_ARGS
req.header: combaseapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IID_PPV_ARGS
 - combaseapi/IID_PPV_ARGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - combaseapi.h
api_name:
 - IID_PPV_ARGS
---

## -description

Used to retrieve an interface pointer, supplying the IID value of the requested interface automatically based on the type of the interface pointer used. This avoids a common coding error by checking the type of the value passed at compile time.

## -parameters

### -param ppType

An address of an interface pointer whose type <b>T</b> is used to determine the type of object being requested. The macro returns the interface pointer through this parameter.

## -remarks

A common syntax in methods that retrieve an interface pointer (most notably <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> and <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>) includes two parameters:

<ul>
<li>An [in] parameter, normally of type <b>REFIID</b>, to specify the IID of the interface to retrieve.</li>
<li>An [out] parameter, normally of type <b>void**</b>, to receive the interface pointer.</li>
</ul>
This macro computes the IID based on the type of interface pointer, which prevents coding errors in which the IID and interface pointer type do not match. Windows developers should always use this macro with any method that requires separate IID and interface pointer parameters.

While Windows 7 is the first inclusion of this macro in a public header, it can be used on older systems by defining it manually in your project headers or source code.

The following example shows the use of <b>IID_PPV_ARGS</b> to create the memory property store object using <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>.

```cpp
IPropertyStore *pPropertyStore;

CoCreateInstance(CLSID_PropertyStore, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pPropertyStore));
```

## -syntax

```cpp
void IID_PPV_ARGS(
    T **ppType
);
```
