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

# tagDDDEVICEIDENTIFIER2 structure


## -description


The <b>DDDEVICEIDENTIFIER2</b> structure is passed to the <a href="https://msdn.microsoft.com/1524dae8-e383-47f4-8e18-c8ef235b3176">IDirectDraw7::GetDeviceIdentifier</a> method to obtain information about a device.


## -struct-fields




### -field szDriver

Name of the driver.


### -field szDescription

Description of the driver.


### -field liDriverVersion

Version of the driver. It is valid to do less than and greater than comparisons on all 64 bits. Caution should be exercised if you use this element to identify problematic drivers; instead, use the <b>guidDeviceIdentifier</b> member for this purpose.

The data takes the following form:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
wProduct = HIWORD(liDriverVersion.HighPart)
wVersion = LOWORD(liDriverVersion.HighPart)
wSubVersion = HIWORD(liDriverVersion.LowPart)
wBuild = LOWORD(liDriverVersion.LowPart)
</pre>
</td>
</tr>
</table></span></div>

### -field dwDriverVersionLowPart

 


### -field dwDriverVersionHighPart

 


### -field dwVendorId

Identifier of the manufacturer. Can be 0 if unknown.


### -field dwDeviceId

Identifier of the type of chipset. Can be 0 if unknown.


### -field dwSubSysId

Identifier of the subsystem. Typically, this means the particular board. Can be 0 if unknown.


### -field dwRevision

Identifier of the revision level of the chipset. Can be 0 if unknown.


### -field guidDeviceIdentifier

Unique identifier for the driver and chipset pair. Use this value if you want to track changes to the driver or chipset to reprofile the graphics subsystem. It can also be used to identify particular problematic drivers.


### -field dwWHQLLevel

The Windows Hardware Quality Lab (WHQL) certification level for the device and driver pair.


## -remarks



The values in <b>szDriver</b> and <b>szDescription</b> are for presentation to the user only. They should not be used to identify particular drivers because different strings might be associated with the same device, or the same driver from different vendors might be described differently.



The <b>dwVendorId</b>, <b>dwDeviceId</b>, <b>dwSubSysId</b>, and <b>dwRevision</b> members can be used to identify particular chipsets, but use extreme caution.





