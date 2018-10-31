---
UID: NF:bits3_0.IEnumBitsPeerCacheRecords.Clone
title: IEnumBitsPeerCacheRecords::Clone
author: windows-sdk-content
description: Creates another IEnumBitsPeerCacheRecords enumerator that contains the same enumeration state as the current one.
old-location: bits\ienumbitspeercacherecords_clone.htm
tech.root: Bits
ms.assetid: 4eb19401-119d-4ce6-92b1-aa41b6dcb97c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Clone, Clone method [BITS], Clone method [BITS],IEnumBitsPeerCacheRecords interface, IEnumBitsPeerCacheRecords interface [BITS],Clone method, IEnumBitsPeerCacheRecords.Clone, IEnumBitsPeerCacheRecords::Clone, bits.ienumbitspeercacherecords_clone, bits3_0/IEnumBitsPeerCacheRecords::Clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IEnumBitsPeerCacheRecords.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumBitsPeerCacheRecords::Clone


## -description


Creates another 
<a href="https://msdn.microsoft.com/680c1468-d780-44a3-9048-c7c3928234f9">IEnumBitsPeerCacheRecords</a> enumerator that contains the same enumeration state as the current one.

Using this method, a client can record a particular point in the enumeration sequence, and then return to that point at a later time. The new enumerator supports the same interface as the original one.


## -parameters




### -param ppenum

TBD




#### - ppEnum [out]

Receives the interface pointer to the enumeration object. If the method is unsuccessful, the value of this output variable is undefined. You must release <i>ppEnum</i> when done.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -see-also




<a href="https://msdn.microsoft.com/680c1468-d780-44a3-9048-c7c3928234f9">IEnumBitsPeerCacheRecords</a>
 

 

