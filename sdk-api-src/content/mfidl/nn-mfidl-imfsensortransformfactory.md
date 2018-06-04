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

# IMFSensorTransformFactory interface


## -description


The interface implemented by sensor transforms to allow  the media pipeline to query requirements of the sensor transform and to create a runtime instance of the sensor transform.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSensorTransformFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSensorTransformFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSensorTransformFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90F986B1-7E1A-43AC-A633-34DD9D53D634">CreateTransform</a>
</td>
<td align="left" width="63%">
Called by the media pipeline to create the transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D1B1DA8D-9A59-43A0-9A2F-8749B2C05D37">GetTransformCount</a>
</td>
<td align="left" width="63%">
Called by the media pipeline to get the number of transforms provided by the sensor transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A83B0A75-60CF-49AA-9386-70A30189C009">GetTransformInformation</a>
</td>
<td align="left" width="63%">
Called by the media pipeline to get information about a transform provided by the  sensor transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/395BC62A-5A20-4C9D-A097-2DBEF6CD93C2">InitializeFactory</a>
</td>
<td align="left" width="63%">
Called by the media pipeline to initialize the sensor transform.

</td>
</tr>
</table> 

