---
UID: NF:bits3_0.IEnumBitsPeers.Clone
title: IEnumBitsPeers::Clone
author: windows-sdk-content
description: Creates another IEnumBitsPeers enumerator that contains the same enumeration state as the current one.
old-location: bits\ienumbitspeers_clone.htm
tech.root: Bits
ms.assetid: 72b3e0bc-9426-4953-a910-2dfaa955c4c0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Clone, Clone method [BITS], Clone method [BITS],IEnumBitsPeers interface, IEnumBitsPeers interface [BITS],Clone method, IEnumBitsPeers.Clone, IEnumBitsPeers::Clone, bits.ienumbitspeers_clone, bits3_0/IEnumBitsPeers::Clone
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
 - IEnumBitsPeers.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumBitsPeers::Clone


## -description


Creates another 
<a href="https://msdn.microsoft.com/2715a58c-ba76-4223-ad9e-453d029e0eda">IEnumBitsPeers</a> enumerator that contains the same enumeration state as the current one.

Using this method, a client can record a particular point in the enumeration sequence, and then return to that point at a later time. The new enumerator supports the same interface as the original one.


## -parameters




### -param ppenum [out]

Receives the interface pointer to the enumeration object. If the method is unsuccessful, the value of this output variable is undefined. You must release <i>ppEnum</i> when done.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -see-also




<a href="https://msdn.microsoft.com/2715a58c-ba76-4223-ad9e-453d029e0eda">IEnumBitsPeers</a>
 

 

