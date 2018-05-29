---
UID: NF:powrprof.PowerSettingAccessCheck
title: PowerSettingAccessCheck function
author: windows-sdk-content
description: Queries for a group policy override for specified power settings.
old-location: base\powersettingaccesscheck.htm
old-project: Power
ms.assetid: 0b89c189-b162-44d4-aa50-d78385e40c27
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: ACCESS_ACTIVE_SCHEME, ACCESS_AC_POWER_SETTING_INDEX, ACCESS_CREATE_SCHEME, ACCESS_DC_POWER_SETTING_INDEX, ACCESS_SCHEME, PowerSettingAccessCheck, PowerSettingAccessCheck function, base.powersettingaccesscheck, powrprof/PowerSettingAccessCheck
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: powrprof.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: POWER_DATA_ACCESSOR, *PPOWER_DATA_ACCESSOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	PowrProf.dll
api_name:
-	PowerSettingAccessCheck
product: Windows
targetos: Windows
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PowerSettingAccessCheck function


## -description


Queries for a group policy override for specified power settings.


## -parameters




### -param AccessFlags [in]

The type of access to check for group policy overrides.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACCESS_AC_POWER_SETTING_INDEX"></a><a id="access_ac_power_setting_index"></a><dl>
<dt><b>ACCESS_AC_POWER_SETTING_INDEX</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
Check for overrides on AC power settings.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_DC_POWER_SETTING_INDEX"></a><a id="access_dc_power_setting_index"></a><dl>
<dt><b>ACCESS_DC_POWER_SETTING_INDEX</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Check for overrides on DC power settings.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_SCHEME"></a><a id="access_scheme"></a><dl>
<dt><b>ACCESS_SCHEME</b></dt>
<dt>16 (0x10)</dt>
</dl>
</td>
<td width="60%">
Check for restrictions on specific power schemes.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_ACTIVE_SCHEME"></a><a id="access_active_scheme"></a><dl>
<dt><b>ACCESS_ACTIVE_SCHEME</b></dt>
<dt>19 (0x13)</dt>
</dl>
</td>
<td width="60%">
Check for restrictions on active power schemes.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_CREATE_SCHEME"></a><a id="access_create_scheme"></a><dl>
<dt><b>ACCESS_CREATE_SCHEME</b></dt>
<dt>20 (0x14)</dt>
</dl>
</td>
<td width="60%">
Check for restrictions on creating or restoring power schemes.

</td>
</tr>
</table>
 


### -param PowerGuid [in, optional]

The identifier of the power setting.


## -returns



Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
The specified power setting is not currently overridden by a group policy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DISABLED_BY_POLICY</b></dt>
<dt>1260 (0x4EC)</dt>
</dl>
</td>
<td width="60%">
This program is blocked by group policy. For more information, contact your system administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_REMOTE_DISALLOWED</b></dt>
<dt>1640 (0x668)</dt>
</dl>
</td>
<td width="60%">
Only Administrators can remotely access power settings.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4b3f8f89-2ade-4594-b055-b1873e74cda6">POWER_DATA_ACCESSOR</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>
 

 

