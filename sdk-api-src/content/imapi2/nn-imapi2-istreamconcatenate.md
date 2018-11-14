---
UID: NN:imapi2.IStreamConcatenate
title: IStreamConcatenate
author: windows-sdk-content
description: Use this interface to combine several data streams into a single stream.
old-location: imapi\istreamconcatenate.htm
tech.root: imapi
ms.assetid: 48b786ef-a1b6-4dcf-9329-c659f15185e1
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IStreamConcatenate, IStreamConcatenate interface [IMAPI], IStreamConcatenate interface [IMAPI],described, imapi.istreamconcatenate, imapi2/IStreamConcatenate
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IStreamConcatenate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStreamConcatenate interface


## -description


Use this interface to combine several data streams into a single stream.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftStreamConcatenate) for the class identifier and __uuidof(IStreamConcatenate) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamConcatenate</b> interface inherits from <b>IStream</b>. <b>IStreamConcatenate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamConcatenate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9871cc35-c955-4fd4-9082-5b6ab60cae7b">Append</a>
</td>
<td align="left" width="63%">
Appends a stream to this stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75e7f4cd-f3c8-494d-b049-7fe32c486659">Append2</a>
</td>
<td align="left" width="63%">
Appends an array of streams to this stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62db148e-926d-47b3-a0f6-945730177184">Initialize</a>
</td>
<td align="left" width="63%">
Initializes this stream from two input streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/826b3157-4cab-4f18-87f2-6635911c03f0">Initialize2</a>
</td>
<td align="left" width="63%">
Initializes this stream from an array of input streams.

</td>
</tr>
</table> 


## -remarks



To create the  MsftStreamConcatenate object in a script, use IMAPI2.MsftStreamConcatenate as the program identifier when calling CreateObject.

When using this interface, the following  scenarios will result in undefined behaviors, and should be avoided:

<ul>
<li>Each partial stream composing the MsftStreamConcatenate object is actually the same stream.</li>
<li>Any of the concatenated streams are modified (read from, written to, or seeked on) outside of IMAPI.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/2d0f03e5-a47d-4b46-a177-f462bbafe153">IStreamInterleave</a>



<a href="https://msdn.microsoft.com/7630b8ac-41f9-4cc7-95e7-4172a876673f">IStreamPseudoRandomBased</a>
 

 

