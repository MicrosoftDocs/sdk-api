---
UID: NN:imapi2.IStreamInterleave
title: IStreamInterleave
author: windows-sdk-content
description: Use this interface to combine several data streams into a single stream by alternately interspersing portions of each.
old-location: imapi\istreaminterleave.htm
old-project: imapi
ms.assetid: 2d0f03e5-a47d-4b46-a177-f462bbafe153
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IStreamInterleave, IStreamInterleave interface [IMAPI], IStreamInterleave interface [IMAPI],described, imapi.istreaminterleave, imapi2/IStreamInterleave
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: imapi2.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IStreamInterleave
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IStreamInterleave interface


## -description


Use this interface to combine several data streams into a single stream by alternately interspersing portions of each. You create interleaved streams when data streams need to run parallel to each other instead of sequentially. For example, some CD formats require user data interleaved with the subcode information. Any fixed-size interleave is supported.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftStreamInterleave) for the class identifier and __uuidof(IStreamInterleave) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamInterleave</b> interface inherits from <b>IStream</b>. <b>IStreamInterleave</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamInterleave</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/889db097-3a16-4c35-9a79-e4a9d8060832">Initialize</a>
</td>
<td align="left" width="63%">
Initializes this interleaved stream from an array of input streams and interleave sizes.

</td>
</tr>
</table> 


## -remarks



To create the <b>MsftStreamInterleave</b> object in a script, use IMAPI2.MsftStreamInterleave as the program identifier when calling <b>CreateObject</b>.




## -see-also




<a href="https://msdn.microsoft.com/48b786ef-a1b6-4dcf-9329-c659f15185e1">IStreamConcatenate</a>



<a href="https://msdn.microsoft.com/7630b8ac-41f9-4cc7-95e7-4172a876673f">IStreamPseudoRandomBased</a>
 

 

