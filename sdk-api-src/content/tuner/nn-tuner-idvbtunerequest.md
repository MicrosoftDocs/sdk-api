---
UID: NN:tuner.IDVBTuneRequest
title: IDVBTuneRequest
author: windows-sdk-content
description: The IDVBTuneRequest interface is implemented on the DVBTuneRequest object.
old-location: mstv\idvbtunerequest.htm
old-project: mstv
ms.assetid: 4d519bbc-38e1-47ce-bd73-a3eb1ea399d6
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IDVBTuneRequest, IDVBTuneRequest interface [Microsoft TV Technologies], IDVBTuneRequest interface [Microsoft TV Technologies],described, IDVBTuneRequestInterface, mstv.idvbtunerequest, tuner/IDVBTuneRequest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IDVBTuneRequest
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBTuneRequest interface


## -description



The <b>IDVBTuneRequest</b> interface is implemented on the <a href="https://msdn.microsoft.com/a2f23290-4836-49d6-9978-e51bdb5c2e15">DVBTuneRequest</a> object. It provides methods for acquiring a transport stream, and a service on that stream, in tuning spaces with a DVB network type. This information is obtained by the Guide Store loader from the TIF, stored in the tune request, and ultimately used by the Network Provider to configure the MPEG-2 Demultiplexer so that the correct packets are decoded and passed on to the downstream filters.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVBTuneRequest</b> interface inherits from <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a>. <b>IDVBTuneRequest</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVBTuneRequest</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24cfc4bb-7df0-4380-9322-4bec6e8a2385">get_ONID</a>
</td>
<td align="left" width="63%">
Retrieves the original network ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ddd5eec-c8bc-4f26-8acd-cf42876345ad">get_SID</a>
</td>
<td align="left" width="63%">
Sets the service ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bbc0fd0-5b4d-4701-b3ca-7581efff9e71">get_TSID</a>
</td>
<td align="left" width="63%">
Retrieves the transport stream ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f080aed-3a25-4464-ab74-27327a9f62a5">put_ONID</a>
</td>
<td align="left" width="63%">
Sets the original network ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f521ab2d-5c56-4aff-a0a3-ac94b8676363">put_SID</a>
</td>
<td align="left" width="63%">
Retrieves the service ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f72dce85-3584-40bc-ae7a-69c9914c13b9">put_TSID</a>
</td>
<td align="left" width="63%">
Sets the transport stream ID.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDVBTuneRequest)</code>.




## -see-also




<a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

