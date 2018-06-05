---
UID: NF:pla.ITraceDataProviderCollection.get__NewEnum
title: ITraceDataProviderCollection::get__NewEnum
author: windows-sdk-content
description: Retrieves an interface to the enumeration.
old-location: pla\itracedataprovidercollection__newenum.htm
old-project: PLA
ms.assetid: cd80839a-0cf0-4553-819e-7a8be830b9fa
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ITraceDataProviderCollection interface [PLA],_NewEnum property, ITraceDataProviderCollection._NewEnum, ITraceDataProviderCollection.get__NewEnum, ITraceDataProviderCollection::_NewEnum, ITraceDataProviderCollection::get__NewEnum, _NewEnum property [PLA], _NewEnum property [PLA],ITraceDataProviderCollection interface, get__NewEnum, pla.itracedataprovidercollection__newenum, pla/ITraceDataProviderCollection::_NewEnum, pla/ITraceDataProviderCollection::get__NewEnum
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
tech.root: 
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	ITraceDataProviderCollection._NewEnum
-	ITraceDataProviderCollection.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITraceDataProviderCollection::get__NewEnum


## -description


Retrieves an interface to the enumeration.

This property is read-only.


## -parameters


## -remarks



 C++ programmers use this property.

The enumeration is a snapshot of the collection at the time of the call.

The items of the enumeration are variants whose type is VT_UNKNOWN. To query for the <a href="https://msdn.microsoft.com/1f57aa92-81f0-445f-baa3-274714e8291e">ITraceDataCollector</a> interface, use the <b>punkVal</b> member of the variant.




## -see-also




<a href="https://msdn.microsoft.com/74300222-dca4-4871-bae3-0c3182fbc539">ITraceDataProviderCollection</a>
 

 

