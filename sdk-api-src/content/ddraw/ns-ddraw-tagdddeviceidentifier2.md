---
UID: NS:ddraw.tagDDDEVICEIDENTIFIER2
title: tagDDDEVICEIDENTIFIER2
author: windows-sdk-content
description: The DDDEVICEIDENTIFIER2 structure is passed to the IDirectDraw7::GetDeviceIdentifier method to obtain information about a device.
old-location: directdraw\dddeviceidentifier2.htm
old-project: directdraw
ms.assetid: 3fdec953-72d4-48f8-b540-e2e6ca770b3c
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: "*LPDDDEVICEIDENTIFIER2, DDDEVICEIDENTIFIER2, DDDEVICEIDENTIFIER2 structure [DirectDraw], LPDDDEVICEIDENTIFIER2, LPDDDEVICEIDENTIFIER2 structure pointer [DirectDraw], ddraw/DDDEVICEIDENTIFIER2, ddraw/LPDDDEVICEIDENTIFIER2, directdraw.dddeviceidentifier2, tagDDDEVICEIDENTIFIER2"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddraw.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: DDDEVICEIDENTIFIER2, *LPDDDEVICEIDENTIFIER2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ddraw.h
api_name:
-	DDDEVICEIDENTIFIER2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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





