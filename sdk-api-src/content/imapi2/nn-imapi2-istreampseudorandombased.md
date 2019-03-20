---
UID: NN:imapi2.IStreamPseudoRandomBased
title: IStreamPseudoRandomBased (imapi2.h)
author: windows-sdk-content
description: Use this interface to generate a read-only data stream whose data is initialized with pseudo-random data (not cryptographically safe). You must call the SetSize method to set the requested size of the stream.
old-location: imapi\istreampseudorandombased.htm
tech.root: imapi
ms.assetid: 7630b8ac-41f9-4cc7-95e7-4172a876673f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IStreamPseudoRandomBased, IStreamPseudoRandomBased interface [IMAPI], IStreamPseudoRandomBased interface [IMAPI],described, imapi.istreampseudorandombased, imapi2/IStreamPseudoRandomBased
ms.topic: interface
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IStreamPseudoRandomBased
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStreamPseudoRandomBased interface


## -description


Use this interface to generate a read-only data stream whose data is initialized with pseudo-random data (not cryptographically safe). You must call the <b>SetSize</b> method to set the requested size of the stream.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use __uuidof(MsftStreamPrng001) for the class identifier and __uuidof(IStreamPseudoRandomBased) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamPseudoRandomBased</b> interface inherits from <b>IStream</b>. <b>IStreamPseudoRandomBased</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamPseudoRandomBased</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e15e47aa-e5c4-4944-a3c4-14e459a31bb5">get_ExtendedSeed</a>
</td>
<td align="left" width="63%">
Retrieves an array of seed values used by the random number generator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5362760-84c6-4e93-b3cd-2ce568b13102">get_Seed</a>
</td>
<td align="left" width="63%">
Retrieves the seed value used by the random number generator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6edf21f-b89a-4780-8065-4d09758fe701">put_ExtendedSeed</a>
</td>
<td align="left" width="63%">
Sets a list of seed values for the random number generator and seeks to the start of stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/455d087d-a6f5-45ab-9c0d-c46e721cba6e">put_Seed</a>
</td>
<td align="left" width="63%">
Sets the seed value used by the random number generator and seeks to the start of stream.

</td>
</tr>
</table> 


## -remarks



To create the <b>MsftStreamPrgn001</b> object in a script, use IMAPI2.MsftStreamPrgn001 as the program identifier when calling <b>CreateObject</b>.




## -see-also




<a href="https://msdn.microsoft.com/48b786ef-a1b6-4dcf-9329-c659f15185e1">IStreamConcatenate</a>



<a href="https://msdn.microsoft.com/2d0f03e5-a47d-4b46-a177-f462bbafe153">IStreamInterleave</a>
 

 

