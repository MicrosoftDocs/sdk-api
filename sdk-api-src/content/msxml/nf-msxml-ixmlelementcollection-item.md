---
UID: NF:msxml.IXMLElementCollection.item
title: IXMLElementCollection::item (msxml.h)
description: Retrieves the child elements from a collection using their index, name, or both.
helpviewer_keywords: ["IXMLElementCollection interface [Windows API]","item method","IXMLElementCollection.item","IXMLElementCollection::item","item","item method [Windows API]","item method [Windows API]","IXMLElementCollection interface","msxml/IXMLElementCollection::item","winprog.ixmlelementcollection_item"]
old-location: winprog\ixmlelementcollection_item.htm
tech.root: winprog
ms.assetid: 3851fe72-b826-4948-ba74-638229429345
ms.date: 12/05/2018
ms.keywords: IXMLElementCollection interface [Windows API],item method, IXMLElementCollection.item, IXMLElementCollection::item, item, item method [Windows API], item method [Windows API],IXMLElementCollection interface, msxml/IXMLElementCollection::item, winprog.ixmlelementcollection_item
req.header: msxml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msxml.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Msxml.tlb
req.lib: 
req.dll: Msxml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXMLElementCollection::item
 - msxml/IXMLElementCollection::item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msxml.dll
api_name:
 - IXMLElementCollection.item
---

# IXMLElementCollection::item


## -description

Retrieves the child elements from a collection using their index, name, or both.

## -parameters

### -param var1 [in, optional]

A valid index numeric value (within the length of <a href="/windows/desktop/api/msxml/nn-msxml-ixmlelementcollection">IXMLElementCollection</a>) or the name of an element in the XML hierarchy.

### -param var2 [in, optional]

A valid index numeric value (within the length of <a href="/windows/desktop/api/msxml/nn-msxml-ixmlelementcollection">IXMLElementCollection</a>) or the name of an element in the XML hierarchy.

### -param ppDisp

TBD

## -returns

Returns an <b>IDispatch</b> pointer to an addressable memory location where the collection is retrievable.

## -remarks

This method is implemented in MSXML 1.0. It is no longer supported by Microsoft in current versions of MSXML. This documentation is provided for informational purposes only.

## -see-also

<a href="/windows/desktop/api/msxml/nn-msxml-ixmlelementcollection">IXMLElementCollection</a>