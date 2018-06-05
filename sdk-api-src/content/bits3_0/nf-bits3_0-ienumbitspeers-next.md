---
UID: NF:bits3_0.IEnumBitsPeers.Next
title: IEnumBitsPeers::Next
author: windows-sdk-content
description: Retrieves a specified number of items in the enumeration sequence. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.
old-location: bits\ienumbitspeers_next.htm
old-project: Bits
ms.assetid: b5bc254d-d74e-4076-a22a-93abf9023068
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IEnumBitsPeers interface [BITS],Next method, IEnumBitsPeers.Next, IEnumBitsPeers::Next, Next, Next method [BITS], Next method [BITS],IEnumBitsPeers interface, bits.ienumbitspeers_next, bits3_0/IEnumBitsPeers::Next
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BG_CERT_STORE_LOCATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Bits.lib
-	Bits.dll
api_name:
-	IEnumBitsPeers.Next
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IEnumBitsPeers::Next


## -description


Retrieves a specified number of items in the enumeration sequence. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.


## -parameters




### -param celt [in]

Number of elements requested.


### -param rgelt [out]

Array of 
<a href="https://msdn.microsoft.com/617b88d4-6c3e-4c33-9bfa-6d9f6f629866">IBitsPeer</a> objects. You must release each object in <i>rgelt</i> when done.


### -param pceltFetched [out]

Number of elements returned in <i>rgelt</i>. You can set <i>pceltFetched</i> to <b>NULL</b> if <i>celt</i> is one. Otherwise, initialize the value of <i>pceltFetched</i> to 0 before calling this method.


## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Successfully returned the number of requested elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Returned less than the number of requested elements.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2715a58c-ba76-4223-ad9e-453d029e0eda">IEnumBitsPeers</a>
 

 

