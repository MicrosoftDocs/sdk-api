---
UID: NF:bits3_0.IEnumBitsPeerCacheRecords.Skip
title: IEnumBitsPeerCacheRecords::Skip
author: windows-sdk-content
description: Skips the next specified number of elements in the enumeration sequence. If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.
old-location: bits\ienumbitspeercacherecords_skip.htm
old-project: Bits
ms.assetid: f1204e4b-985e-4d3e-8a1f-d13d46e8f1ce
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IEnumBitsPeerCacheRecords interface [BITS],Skip method, IEnumBitsPeerCacheRecords.Skip, IEnumBitsPeerCacheRecords::Skip, Skip, Skip method [BITS], Skip method [BITS],IEnumBitsPeerCacheRecords interface, bits.ienumbitspeercacherecords_skip, bits3_0/IEnumBitsPeerCacheRecords::Skip
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
-	IEnumBitsPeerCacheRecords.Skip
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IEnumBitsPeerCacheRecords::Skip


## -description


Skips the next specified number of elements in the enumeration sequence. If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.


## -parameters




### -param celt [in]

Number of elements to skip.


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
Successfully skipped the number of requested elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Skipped less than the number of requested elements.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/680c1468-d780-44a3-9048-c7c3928234f9">IEnumBitsPeerCacheRecords</a>
 

 

