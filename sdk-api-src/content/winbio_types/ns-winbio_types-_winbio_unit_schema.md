---
UID: NS:winbio_types._WINBIO_UNIT_SCHEMA
title: "_WINBIO_UNIT_SCHEMA"
author: windows-driver-content
description: Describes the capabilities of a biometric unit.
old-location: secbiomet\winbio_unit_schema.htm
old-project: SecBioMet
ms.assetid: b20adf18-2948-481f-9d12-8da17aa152f7
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWINBIO_UNIT_SCHEMA, PWINBIO_UNIT_SCHEMA, PWINBIO_UNIT_SCHEMA structure pointer [Windows Biometric Framework API], WINBIO_POOL_PRIVATE, WINBIO_POOL_SYSTEM, WINBIO_POOL_UNKNOWN, WINBIO_UNIT_SCHEMA, WINBIO_UNIT_SCHEMA structure [Windows Biometric Framework API], _WINBIO_UNIT_SCHEMA, secbiomet.winbio_unit_schema, winbio_types/PWINBIO_UNIT_SCHEMA, winbio_types/WINBIO_UNIT_SCHEMA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winbio_types.h
req.include-header: Winbio.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WINBIO_UNIT_SCHEMA, *PWINBIO_UNIT_SCHEMA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winbio_types.h
api_name:
-	WINBIO_UNIT_SCHEMA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_UNIT_SCHEMA structure


## -description


The <b>WINBIO_UNIT_SCHEMA</b> structure describes the capabilities of a biometric unit. It is used by the <a href="https://msdn.microsoft.com/e1ca5712-978e-4e31-a941-eb462c670eac">WinBioEnumBiometricUnits</a> function.


## -struct-fields




### -field UnitId

A value that identifies the biometric unit.


### -field PoolType

A <b>ULONG</b> value that specifies the type of the biometric unit. This can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_POOL_UNKNOWN"></a><a id="winbio_pool_unknown"></a><dl>
<dt><b>WINBIO_POOL_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The type is unknown.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_POOL_SYSTEM"></a><a id="winbio_pool_system"></a><dl>
<dt><b>WINBIO_POOL_SYSTEM</b></dt>
</dl>
</td>
<td width="60%">
The session connects to a shared collection of biometric units managed by the service provider.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_POOL_PRIVATE"></a><a id="winbio_pool_private"></a><dl>
<dt><b>WINBIO_POOL_PRIVATE</b></dt>
</dl>
</td>
<td width="60%">
The session connects to a collection of biometric units that are managed by the caller.

</td>
</tr>
</table>
 


### -field BiometricFactor

A value that specifies the type of the biometric unit. Only <b>WINBIO_TYPE_FINGERPRINT</b> is currently supported.


### -field SensorSubType

A sensor subtype defined for the biometric type specified by the <b>BiometricFactor</b> member. Only  fingerprint types (<b>WINBIO_TYPE_FINGERPRINT</b>) are currently supported. The following subtypes are currently defined for fingerprints:

<ul>
<li>WINBIO_SENSOR_SUBTYPE_UNKNOWN</li>
<li>WINBIO_FP_SENSOR_SUBTYPE_SWIPE</li>
<li>WINBIO_FP_SENSOR_SUBTYPE_TOUCH</li>
</ul>

### -field Capabilities

A bitmask of the biometric sensor capabilities. This can be a bitwise <b>OR</b> of the following values:

<ul>
<li>WINBIO_CAPABILITY_SENSOR</li>
<li>WINBIO_CAPABILITY_MATCHING</li>
<li>WINBIO_CAPABILITY_DATABASE</li>
<li>WINBIO_CAPABILITY_PROCESSING</li>
<li>WINBIO_CAPABILITY_ENCRYPTION</li>
<li>WINBIO_CAPABILITY_NAVIGATION</li>
<li>WINBIO_CAPABILITY_INDICATOR</li>
<li>WINBIO_CAPABILITY_VIRTUAL_SENSOR<div class="alert"><b>Note</b>  The <b>WINBIO_CAPABILITY_VIRTUAL_SENSOR</b> constant applies only for Windows 10 and later.</div>
<div> </div>
</li>
</ul>

### -field DeviceInstanceId

A string value that contains the device ID. The string can contain up to 256 Unicode characters including a terminating <b>NULL</b> character.


### -field Description

A string value that contains a description of the biometric unit. The string can contain up to 256 Unicode characters including a terminating <b>NULL</b> character.


### -field Manufacturer

A string value that contains the name of the manufacturer. The string can contain up to 256 Unicode characters including a terminating <b>NULL</b> character.


### -field Model

A string value that contains the model number of the biometric unit. The string can contain up to 256 Unicode characters including a terminating <b>NULL</b> character.


### -field SerialNumber

A <b>NULL</b>-terminated Unicode string that contains the serial number of the biometric unit. The string can contain up to 256 Unicode characters including a terminating <b>NULL</b> character.


### -field FirmwareVersion

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff536481">WINBIO_VERSION</a> structure that contains the major and minor version numbers for the biometric unit.


## -see-also




<a href="https://msdn.microsoft.com/ac13910c-0c33-4fb8-a9c6-a2d5b1b28c73">Client Application Structures</a>



<a href="https://msdn.microsoft.com/e1ca5712-978e-4e31-a941-eb462c670eac">WinBioEnumBiometricUnits</a>
 

 

