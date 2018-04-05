---
UID: NS:d3d9types._D3DADAPTER_IDENTIFIER9
title: "_D3DADAPTER_IDENTIFIER9"
author: windows-driver-content
description: Contains information identifying the adapter.
old-location: direct3d9\d3dadapter_identifier9.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dadapter_identifier9.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 458ca567-ccb1-1676-d7b3-d971fdd8f312, D3DADAPTER_IDENTIFIER9, D3DADAPTER_IDENTIFIER9 structure [Direct3D 9], LPD3DADAPTER_IDENTIFIER9, LPD3DADAPTER_IDENTIFIER9 structure pointer [Direct3D 9], _D3DADAPTER_IDENTIFIER9, d3d9types/D3DADAPTER_IDENTIFIER9, d3d9types/LPD3DADAPTER_IDENTIFIER9, direct3d9.d3dadapter_identifier9
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d9types.h
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
req.typenames: D3DADAPTER_IDENTIFIER9
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DADAPTER_IDENTIFIER9
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DADAPTER_IDENTIFIER9 structure


## -description


Contains information identifying the adapter.


## -struct-fields




### -field Driver

Type: <b>char</b>

Used for presentation to the user. This should not be used to identify particular drivers, because many different strings might be associated with the same device and driver from different vendors.


### -field Description

Type: <b>char</b>

Used for presentation to the user.


### -field DeviceName

Type: <b>char</b>

Device name for GDI.


### -field DriverVersion

Type: <b><a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a></b>

Identify the version of the Direct3D driver. It is legal to do less than and greater than comparisons on the 64-bit signed integer value. However, exercise caution if you use this element to identify problematic drivers. Instead, you should use DeviceIdentifier. See Remarks.


### -field DriverVersionLowPart

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Identify the version of the Direct3D driver. It is legal to do &lt; and &gt; comparisons on the 64-bit signed integer value. However, exercise caution if you use this element to identify problematic drivers. Instead, you should use DeviceIdentifier. See Remarks.


### -field DriverVersionHighPart

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Identify the version of the Direct3D driver. It is legal to do &lt; and &gt; comparisons on the 64-bit signed integer value. However, exercise caution if you use this element to identify problematic drivers. Instead, you should use DeviceIdentifier. See Remarks.


### -field VendorId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Can be used to help identify a particular chip set. Query this member to identify the manufacturer. The value can be zero if unknown.


### -field DeviceId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Can be used to help identify a particular chip set. Query this member to identify the type of chip set. The value can be zero if unknown.


### -field SubSysId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Can be used to help identify a particular chip set. Query this member to identify the subsystem, typically the particular board. The value can be zero if unknown.


### -field Revision

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Can be used to help identify a particular chip set. Query this member to identify the revision level of the chip set. The value can be zero if unknown.


### -field DeviceIdentifier

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a></b>

Can be queried to check changes in the driver and chip set. This GUID is a unique identifier for the driver and chip set pair. Query this member to track changes to the driver and chip set in order to generate a new profile for the graphics subsystem. DeviceIdentifier can also be used to identify particular problematic drivers.


### -field WHQLLevel

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Used to determine the Windows Hardware Quality Labs (WHQL) validation level for this driver and device pair. The DWORD is a packed date structure defining the date of the release of the most recent WHQL test passed by the driver. It is legal to perform &lt; and &gt; operations on this value. The following illustrates the date format.

<table>
<tr>
<td>Bits</td>
<td></td>
</tr>
<tr>
<td>31-16</td>
<td>The year, a decimal number from 1999 upwards.</td>
</tr>
<tr>
<td>15-8</td>
<td>The month, a decimal number from 1 to 12.</td>
</tr>
<tr>
<td>7-0</td>
<td>The day, a decimal number from 1 to 31.</td>
</tr>
</table>
 

The following values are also used.

<table>
<tr>
<td>0</td>
<td>Not certified.</td>
</tr>
<tr>
<td>1</td>
<td>WHQL validated, but no date information is available.</td>
</tr>
</table>
 

Differences between Direct3D 9 and Direct3D 9Ex:

For Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system), <a href="https://msdn.microsoft.com/aa12e943-9a2c-4c47-be28-7a46f8cb03a9">IDirect3D9::GetAdapterIdentifier</a> returns 1 for the WHQL level without checking the status of the driver. 


## -remarks



The following pseudocode example illustrates the version format encoded in the DriverVersion, DriverVersionLowPart, and DriverVersionHighPart members.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
</pre>
</td>
</tr>
</table></span></div>
See the Platform SDK for more information about the HIWORD macro, the LOWORD macro, and the LARGE_INTEGER structure.

MAX_DEVICE_IDENTIFIER_STRING is a constant with the following definition.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>#define MAX_DEVICE_IDENTIFIER_STRING        512</pre>
</td>
</tr>
</table></span></div>
The VendorId, DeviceId, SubSysId, and Revision members can be used in tandem to identify particular chip sets. However, use these members with caution.




## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>
 

 

