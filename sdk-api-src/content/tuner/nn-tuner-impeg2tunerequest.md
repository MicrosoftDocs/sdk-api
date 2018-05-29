---
UID: NN:tuner.IMPEG2TuneRequest
title: IMPEG2TuneRequest
author: windows-sdk-content
description: The IMPEG2TuneRequest interface represents a tune request for a basic MPEG-2 transport stream containing the minimal tables.Use the IMPEG2TuneRequestFactory::CreateTuneRequest method to obtain this interface.
old-location: mstv\impeg2tunerequest.htm
old-project: mstv
ms.assetid: a9e37b8b-9272-43c6-b36e-1e82b0d1b0db
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMPEG2TuneRequest, IMPEG2TuneRequest interface [Microsoft TV Technologies], IMPEG2TuneRequest interface [Microsoft TV Technologies],described, IMPEG2TuneRequestInterface, mstv.impeg2tunerequest, tuner/IMPEG2TuneRequest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IMPEG2TuneRequest
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IMPEG2TuneRequest interface


## -description



The <b>IMPEG2TuneRequest</b> interface represents a tune request for a basic MPEG-2 transport stream containing the minimal tables.

Use the <a href="https://msdn.microsoft.com/41e299d6-492e-40b4-955f-603b18da0c02">IMPEG2TuneRequestFactory::CreateTuneRequest</a> method to obtain this interface. It returns the minimal MPEG-2 tune request for a specified tuning space. To create a full tune request, use the <b>CreateTuneRequest</b> method provided by one of the tuning space objects.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMPEG2TuneRequest</b> interface inherits from <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a>. <b>IMPEG2TuneRequest</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMPEG2TuneRequest</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dde8979a-633d-4fc4-b31e-bdd43823db6a">get_ProgNo</a>
</td>
<td align="left" width="63%">
Retrieves the program number ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/971e2643-e68f-4b4c-86e0-2e20e2f8a88c">get_TSID</a>
</td>
<td align="left" width="63%">
Retrieves the transport stream ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08fc9cc1-52b7-4782-96a1-af00a76ff6c6">put_ProgNo</a>
</td>
<td align="left" width="63%">
Sets the program number ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47212dc7-601e-4b38-953e-a6b84e73fafa">put_TSID</a>
</td>
<td align="left" width="63%">
Sets the transport stream ID.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2TuneRequest)</code>.




## -see-also




<a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

