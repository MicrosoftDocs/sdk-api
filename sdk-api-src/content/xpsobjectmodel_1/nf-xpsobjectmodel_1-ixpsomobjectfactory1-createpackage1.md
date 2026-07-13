---
UID: NF:xpsobjectmodel_1.IXpsOMObjectFactory1.CreatePackage1
title: IXpsOMObjectFactory1::CreatePackage1
description: The IXpsOMObjectFactory1::CreatePackage1 method (xpsobjectmodel_1.h) creates an IXpsOMPackage1 interface that serves as the root node of an XPS object model document tree.
ms.date: 08/16/2022
ms.topic: language-reference
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: xpsobjectmodel_1.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - xpsobjectmodel_1.h
api_name:
 - IXpsOMObjectFactory1::CreatePackage1
f1_keywords:
 - xpsobjectmodel_1/IXpsOMObjectFactory1::CreatePackage1
dev_langs:
 - c++
---

## -description

Creates an [IXpsOMPackage1](nn-xpsobjectmodel_1-ixpsompackage1.md) interface that serves as the root node of an XPS object model document tree.

## -parameters

### -param package

A pointer to the new [IXpsOMPackage1](nn-xpsobjectmodel_1-ixpsompackage1.md) interface.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, those in the table that follows. For information about XPS document API return values that are not listed in this table, see XPS Document Errors.
| Return code | Description           |
|-------------|-----------------------|
| S_OK        | The method succeeded. |
| E_POINTER   | *package* is NULL.    |

## -remarks

## -see-also

[Create a Blank XPS OM](https://docs.microsoft.com/previous-versions/windows/desktop/dd316970(v=vs.85))

[IXpsOMObjectFactory1](nn-xpsobjectmodel_1-ixpsomobjectfactory1.md)

[IXpsOMPackage1](nn-xpsobjectmodel_1-ixpsompackage1.md)

[XML Paper Specification](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification)

[XPS Document Errors](https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85))