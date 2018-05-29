---
UID: NF:pla.IValueMap.get__NewEnum
title: IValueMap::get__NewEnum
author: windows-sdk-content
description: Retrieves an interface to the enumeration.
old-location: pla\ivaluemap__newenum.htm
old-project: PLA
ms.assetid: 1d40104c-c0a4-41d2-8427-364c37b52e02
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IValueMap interface [PLA],_NewEnum property, IValueMap._NewEnum, IValueMap.get__NewEnum, IValueMap::_NewEnum, IValueMap::get__NewEnum, _NewEnum property [PLA], _NewEnum property [PLA],IValueMap interface, get__NewEnum, pla.ivaluemap__newenum, pla/IValueMap::_NewEnum, pla/IValueMap::get__NewEnum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	IValueMap._NewEnum
-	IValueMap.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IValueMap::get__NewEnum


## -description


Retrieves an interface to the enumeration.

This property is read-only.


## -parameters


## -remarks



 C++ programmers use this property.

The enumeration is a snapshot of the collection at the time of the call.

The items of the enumeration are variants whose type is VT_UNKNOWN. To query for the <a href="https://msdn.microsoft.com/5fab2a62-d974-49f7-ac81-c704d9d8624c">IValueMapItem</a> interface, use the <b>punkVal</b> member of the variant.




## -see-also




<a href="https://msdn.microsoft.com/a7134395-91c6-4ea1-8b76-63830048289f">IValueMap</a>
 

 

