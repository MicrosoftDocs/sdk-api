---
UID: NN:tuner.IDVBTLocator
title: IDVBTLocator
author: windows-driver-content
description: The IDVBTLocator interface is implemented on the DVBTLocator object.
old-location: mstv\idvbtlocator.htm
old-project: mstv
ms.assetid: f5a95a68-fee0-404c-b9c6-6b808977f8d2
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IDVBTLocator, IDVBTLocator interface [Microsoft TV Technologies], IDVBTLocator interface [Microsoft TV Technologies], described, IDVBTLocatorInterface, mstv.idvbtlocator, tuner/IDVBTLocator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tuner.h
req.include-header: 
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IDVBTLocator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBTLocator interface


## -description



The <b>IDVBTLocator</b> interface is implemented on the <a href="https://msdn.microsoft.com/3f37be3e-292f-43f1-aab9-a9b62b259daa">DVBTLocator</a> object. It provides methods to enable a tuner to acquire a terrestrial DVB (DVB-T) transport stream. The data types are defined in Bdatypes.h. Locator data is meant for consumption by the BDA hardware drivers. Applications do not need to interpret any of this data except perhaps for some debugging purposes.

Locators can be created dynamically when the tune request is created, by a loader that has access to the necessary information about the tuning space, or a default locator can be installed when the tuning space is first installed, and the loader can use the default locator when creating tune requests. Applications do not need to use any of the Locator interfaces unless they are creating tune requests. All Locator objects also support <b>IPersistPropertyBag</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVBTLocator</b> interface inherits from <a href="https://msdn.microsoft.com/9af4d871-c6ed-479b-ba41-2a719d3a394d">IDigitalLocator</a>. <b>IDVBTLocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVBTLocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7483d876-fdcc-4eee-b4f3-338846a159c0">get_Bandwidth</a>
</td>
<td align="left" width="63%">
Retrieves the bandwidth of the frequency in megahertz, usually 7 or 8.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74b56292-eb9e-4c66-9345-f348b3d21c19">get_Guard</a>
</td>
<td align="left" width="63%">
Retrieves the guard interval.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/523222c3-ae40-4eed-af22-6cba56df4959">get_HAlpha</a>
</td>
<td align="left" width="63%">
Retrieves the hierarchy alpha.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/069904ad-5faa-4ac4-bf30-538284de2de8">get_LPInnerFEC</a>
</td>
<td align="left" width="63%">
Retrieves the inner FEC type of the low-priority stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eeed8fe6-774d-4375-9b3c-ebe979cd11dd">get_LPInnerFECRate</a>
</td>
<td align="left" width="63%">
Retrieves the inner FEC rate of the low-priority stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1896ca9d-fb43-49eb-88a7-c6217d468a2b">get_Mode</a>
</td>
<td align="left" width="63%">
Receives the transmission mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fcb39760-901f-4c62-a517-bee7ea96f8d9">get_OtherFrequencyInUse</a>
</td>
<td align="left" width="63%">
Indicates whether the frequency is being used by another DVB-T broadcaster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a842e905-cd4a-4d62-a9da-153832e44382">put_Bandwidth</a>
</td>
<td align="left" width="63%">
Sets the bandwidth of the frequency in megahertz, usually 7 or 8.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af0accaf-ef33-4074-ac04-2bd09f3ad879">put_Guard</a>
</td>
<td align="left" width="63%">
Sets the guard interval.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f444c28-972e-4e90-ad99-8bc4f4ee25b7">put_HAlpha</a>
</td>
<td align="left" width="63%">
Sets the hierarchy alpha.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37b5b063-a0ae-4ef8-a63b-44c009a31eb8">put_LPInnerFEC</a>
</td>
<td align="left" width="63%">
Sets the inner FEC type of the low-priority stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4fcce13b-1cc4-4ee7-b010-2c5ffd55a5f7">put_LPInnerFECRate</a>
</td>
<td align="left" width="63%">
Sets the inner FEC rate of the low-priority stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/762f4604-46c9-4c19-9621-5ede52d8f524">put_Mode</a>
</td>
<td align="left" width="63%">
Sets the transmission mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab9504f9-469d-476d-aad8-f9534f6b41bf">put_OtherFrequencyInUse</a>
</td>
<td align="left" width="63%">
Specifies whether the frequency is being used by another DVB-T broadcaster.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDVBTLocator)</code>.




## -see-also




<a href="https://msdn.microsoft.com/9af4d871-c6ed-479b-ba41-2a719d3a394d">IDigitalLocator</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

