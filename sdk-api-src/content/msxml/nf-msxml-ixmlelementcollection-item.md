---
UID: NF:msxml.IXMLElementCollection.item
title: IXMLElementCollection::item
author: windows-sdk-content
description: Retrieves the child elements from a collection using their index, name, or both.
old-location: winprog\ixmlelementcollection_item.htm
tech.root: devnotes
ms.assetid: 3851fe72-b826-4948-ba74-638229429345
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IXMLElementCollection interface [Windows API],item method, IXMLElementCollection.item, IXMLElementCollection::item, item, item method [Windows API], item method [Windows API],IXMLElementCollection interface, msxml/IXMLElementCollection::item, winprog.ixmlelementcollection_item
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msxml.dll
api_name:
 - IXMLElementCollection.item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXMLElementCollection::item


## -description


Retrieves the child elements from a collection using their index, name, or both.


## -parameters




### -param var1 [in, optional]

A valid index numeric value (within the length of <a href="https://msdn.microsoft.com/1d27e5fc-0491-44ee-9134-40f9f909b1cb">IXMLElementCollection</a>) or the name of an element in the XML hierarchy.


### -param var2 [in, optional]

A valid index numeric value (within the length of <a href="https://msdn.microsoft.com/1d27e5fc-0491-44ee-9134-40f9f909b1cb">IXMLElementCollection</a>) or the name of an element in the XML hierarchy.


### -param ppDisp

TBD




## -returns



Returns an <b>IDispatch</b> pointer to an addressable memory location where the collection is retrievable.




## -remarks



This method is implemented in MSXML 1.0. It is no longer supported by Microsoft in current versions of MSXML. This documentation is provided for informational purposes only.




## -see-also




<a href="https://msdn.microsoft.com/1d27e5fc-0491-44ee-9134-40f9f909b1cb">IXMLElementCollection</a>
 

 

