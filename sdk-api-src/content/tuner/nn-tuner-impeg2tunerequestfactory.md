---
UID: NN:tuner.IMPEG2TuneRequestFactory
title: IMPEG2TuneRequestFactory
author: windows-driver-content
description: The IMPEG2TuneRequestFactory interface creates a tune request for a basic MPEG-2 transport stream containing the minimal tables. To obtain this interface, call CoCreateInstance with the class identifier CLSID_MPEG2TuneRequestFactory.
old-location: mstv\impeg2tunerequestfactory.htm
old-project: mstv
ms.assetid: 0fbeab7d-0c54-45e3-a73c-755df28a16d5
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMPEG2TuneRequestFactory, IMPEG2TuneRequestFactory interface [Microsoft TV Technologies], IMPEG2TuneRequestFactory interface [Microsoft TV Technologies], described, IMPEG2TuneRequestFactoryInterface, mstv.impeg2tunerequestfactory, tuner/IMPEG2TuneRequestFactory
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IMPEG2TuneRequestFactory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IMPEG2TuneRequestFactory interface


## -description



The <b>IMPEG2TuneRequestFactory</b> interface creates a tune request for a basic MPEG-2 transport stream containing the minimal tables. To obtain this interface, call <b>CoCreateInstance</b> with the class identifier CLSID_MPEG2TuneRequestFactory.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMPEG2TuneRequestFactory</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMPEG2TuneRequestFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMPEG2TuneRequestFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41e299d6-492e-40b4-955f-603b18da0c02">CreateTuneRequest</a>
</td>
<td align="left" width="63%">
Creates the minimal MPEG-2 tune request for a specified tuning space

</td>
</tr>
</table> 


## -remarks




        To create a full tune request, use the <a href="https://msdn.microsoft.com/b22ccd86-b8d7-4dd7-af4b-b99c9fea0de5">CreateTuneRequest</a> method provided by one of the tuning space objects.
      

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2TuneRequestFactory)</code>.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

