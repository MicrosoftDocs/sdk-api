---
UID: NF:xpsobjectmodel_1.IXpsOMObjectFactory1.CreatePage1
title: IXpsOMObjectFactory1::CreatePage1
description: The IXpsOMObjectFactory1::CreatePage1 method (xpsobjectmodel_1.h) creates an IXpsOMPage interface, which provides the root node of a tree of objects that represent the contents of a single page.
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
 - IXpsOMObjectFactory1::CreatePage1
f1_keywords:
 - xpsobjectmodel_1/IXpsOMObjectFactory1::CreatePage1
dev_langs:
 - c++
---

## -description

Creates an [IXpsOMPage](nn-xpsobjectmodel_1-ixpsompage1.md) interface,  which provides the root node of a tree of objects  that represent the contents of a single page.

## -parameters

### -param pageDimensions

The [XPS_SIZE](https://docs.microsoft.com/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size) structure that specifies the size of the page to be created.

Size is described in XPS units. There are 96 XPS units per inch.  For example, the dimensions of an 8.5" by 11.0" page are 816 by 1,056 XPS units.

### -param language

The string that indicates the default language of the created page.

> [!ALERT]
> **Important**  The language string must follow the RFC 3066 syntax.

### -param partUri

The [IOpcPartUri](https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) interface that contains the part name to be assigned to this resource.

### -param page

A pointer to the new [IXpsOMPage](nn-xpsobjectmodel_1-ixpsompage1.md) interface.

## -returns

The method returns an **HRESULT**. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see [XPS Document Errors](https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)).

| Return code             | Description                                                                  |
|-------------------------|------------------------------------------------------------------------------|
| S_OK                    | The method succeeded.                                                        |
| E_POINTER               | **pageDimensions**, **partUri**, or **page** is **NULL**.                    |
| XPS_E_INVALID_LANGUAGE  | **language** does not contain a valid language string.                       |
| XPS_E_INVALID_PAGE_SIZE |**pageDimensions** contains an invalid page size or invalid page size values. |

## -remarks

## -see-also

[IXpsOMObjectFactory1](nn-xpsobjectmodel_1-ixpsomobjectfactory1.md)

[The Internet Engineering Task Force (IETF) RFC 3066](https://go.microsoft.com/fwlink/p/?linkid=161490)

[XML Paper Specification](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification)

[XML Paper Specification](https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85))
