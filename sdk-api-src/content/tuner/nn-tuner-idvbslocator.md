---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDVBSLocator interface


## -description



The <b>IDVBSLocator</b> interface is implemented on the <a href="https://msdn.microsoft.com/ef3e2752-ee37-478c-8f2f-4bd6262f7cf2">DVBSLocator</a> object. It provides information to enable a tuner to acquire a satellite DVB (DVB-S) transmission. The methods for acquiring a transport stream once the signal is tuned are provided by IDVBTuneRequest. Locator data is meant for consumption by the BDA hardware drivers. Applications do not need to interpret any of this data except perhaps for some debugging purposes.

Locators can be created dynamically when the tune request is created, by a loader that has access to the necessary information about the tuning space, or a default locator can be installed when the tuning space is first installed, and the loader can use the default locator when creating tune requests. Applications do not need to use any of the Locator interfaces unless they are creating tune requests. All Locator objects also support <b>IPersistPropertyBag</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVBSLocator</b> interface inherits from <a href="https://msdn.microsoft.com/9af4d871-c6ed-479b-ba41-2a719d3a394d">IDigitalLocator</a>. <b>IDVBSLocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVBSLocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c1314f4-6291-4440-8010-247f8fa82d0c">get_Azimuth</a>
</td>
<td align="left" width="63%">
Retrieves the azimuth setting used for positioning the satellite dish.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d81cb6d-412f-4a55-b9fc-a0a0e8cebaaa">get_Elevation</a>
</td>
<td align="left" width="63%">
Retrieves the elevation of the satellite in tenths of a degree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3069cf27-32db-4d3f-9e61-9eddc266b540">get_OrbitalPosition</a>
</td>
<td align="left" width="63%">
Retrieves the setting for the satellite's orbital position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adb9d7b6-5876-4b3f-9d82-f5e740feb1eb">get_SignalPolarisation</a>
</td>
<td align="left" width="63%">
Retrieves the signal polarisation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97bb32ba-02ca-4ea4-8364-6edddbb05d8c">get_WestPosition</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the orbital position is given in east or west longitude.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4923fa80-77f7-4d2e-9a15-ce7608888e02">put_Azimuth</a>
</td>
<td align="left" width="63%">
Adjusts the azimuth setting used for positioning the satellite dish.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12db3e20-9102-483c-a4ef-8a90a376b7af">put_Elevation</a>
</td>
<td align="left" width="63%">
Sets the elevation of the satellite in tenths of a degree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2de4d67c-5d99-47c2-99bf-e4f40c6247a5">put_OrbitalPosition</a>
</td>
<td align="left" width="63%">
Sets the setting for the satellite's orbital position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc94c956-6895-451a-8d1c-2001a6fbec63">put_SignalPolarisation</a>
</td>
<td align="left" width="63%">
Sets the signal polarisation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/567aa90e-6179-477a-813d-13e99b16bbc2">put_WestPosition</a>
</td>
<td align="left" width="63%">
Sets the longitudinal position as west longitude or east longitude.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDVBSLocator)</code>.




## -see-also




<a href="https://msdn.microsoft.com/9af4d871-c6ed-479b-ba41-2a719d3a394d">IDigitalLocator</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

