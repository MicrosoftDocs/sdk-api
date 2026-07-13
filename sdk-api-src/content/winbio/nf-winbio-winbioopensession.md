---
UID: NF:winbio.WinBioOpenSession
title: WinBioOpenSession function (winbio.h)
description: Connects to a biometric service provider and one or more biometric units.
helpviewer_keywords: ["WINBIO_DB_BOOTSTRAP","WINBIO_DB_DEFAULT","WINBIO_DB_ONCHIP","WINBIO_FLAG_ADVANCED","WINBIO_FLAG_BASIC","WINBIO_FLAG_DEFAULT","WINBIO_FLAG_MAINTENANCE","WINBIO_FLAG_RAW","WINBIO_POOL_PRIVATE","WINBIO_POOL_SYSTEM","WinBioOpenSession","WinBioOpenSession function [Windows Biometric Framework API]","secbiomet.winbioopensession","winbio/WinBioOpenSession"]
old-location: secbiomet\winbioopensession.htm
tech.root: SecBioMet
ms.assetid: e9a0bb5f-4bbd-4dc4-9cd8-c26f5e4f74cf
ms.date: 12/05/2018
ms.keywords: WINBIO_DB_BOOTSTRAP, WINBIO_DB_DEFAULT, WINBIO_DB_ONCHIP, WINBIO_FLAG_ADVANCED, WINBIO_FLAG_BASIC, WINBIO_FLAG_DEFAULT, WINBIO_FLAG_MAINTENANCE, WINBIO_FLAG_RAW, WINBIO_POOL_PRIVATE, WINBIO_POOL_SYSTEM, WinBioOpenSession, WinBioOpenSession function [Windows Biometric Framework API], secbiomet.winbioopensession, winbio/WinBioOpenSession
req.header: winbio.h
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
req.lib: Winbio.lib
req.dll: Winbio.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinBioOpenSession
 - winbio/WinBioOpenSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winbio.dll
 - Ext-MS-Win-BioMetrics-WinBio-l1-2-0.dll
 - winbioext.dll
 - Ext-MS-Win-BioMetrics-WinBio-L1-3-0.dll
api_name:
 - WinBioOpenSession
---

# WinBioOpenSession function


## -description

Connects to a biometric service provider and one or more biometric units.

## -parameters

### -param Factor [in]

A bitmask of <a href="/windows-hardware/drivers/ddi/content/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes">WINBIO_BIOMETRIC_TYPE</a> flags that specifies the biometric unit types to be enumerated. Only <b>WINBIO_TYPE_FINGERPRINT</b> is currently supported.

### -param PoolType [in]

A <b>ULONG</b> value that specifies the type of the biometric units that will be used in the session. This can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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

### -param Flags [in]

A <b>ULONG</b> value that specifies biometric unit configuration and access characteristics for the new session. Configuration flags specify the general configuration of units in the session. Access flags specify how the application will use the biometric units. You must specify one configuration flag but you can combine that flag with any access flag.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_FLAG_DEFAULT"></a><a id="winbio_flag_default"></a><dl>
<dt><b>WINBIO_FLAG_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Group: configuration

The biometric units operate in the manner specified during installation. You must use this value when the <i>PoolType</i> parameter is WINBIO_POOL_SYSTEM.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_FLAG_BASIC"></a><a id="winbio_flag_basic"></a><dl>
<dt><b>WINBIO_FLAG_BASIC</b></dt>
</dl>
</td>
<td width="60%">
Group: configuration

The biometric units operate only as basic capture devices. All processing, matching, and storage operations is performed by software plug-ins.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_FLAG_ADVANCED"></a><a id="winbio_flag_advanced"></a><dl>
<dt><b>WINBIO_FLAG_ADVANCED</b></dt>
</dl>
</td>
<td width="60%">
Group: configuration

The biometric units use internal processing and storage capabilities.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_FLAG_RAW"></a><a id="winbio_flag_raw"></a><dl>
<dt><b>WINBIO_FLAG_RAW</b></dt>
</dl>
</td>
<td width="60%">
Group: access

The client application captures raw biometric data using <a href="/windows/desktop/api/winbio/nf-winbio-winbiocapturesample">WinBioCaptureSample</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_FLAG_MAINTENANCE"></a><a id="winbio_flag_maintenance"></a><dl>
<dt><b>WINBIO_FLAG_MAINTENANCE</b></dt>
</dl>
</td>
<td width="60%">
Group: access

The client performs vendor-defined control operations on a biometric unit by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbiocontrolunitprivileged">WinBioControlUnitPrivileged</a>.

</td>
</tr>
</table>

### -param UnitArray [in]

Pointer to an array of biometric unit identifiers to be included in the session. You can call <a href="/windows/desktop/api/winbio/nf-winbio-winbioenumbiometricunits">WinBioEnumBiometricUnits</a> to enumerate the biometric units. Set this value to <b>NULL</b> if the <i>PoolType</i> parameter is <b>WINBIO_POOL_SYSTEM</b>.

### -param UnitCount [in]

A value that specifies the number of elements in the array pointed to by the <i>UnitArray</i> parameter. Set this value to zero if the <i>PoolType</i> parameter is <b>WINBIO_POOL_SYSTEM</b>.

### -param DatabaseId [in]

A value that specifies the database(s) to be used by the session. If the <i>PoolType</i> parameter is <b>WINBIO_POOL_PRIVATE</b>, you must specify the GUID of an installed database.  If the <i>PoolType</i> parameter is not <b>WINBIO_POOL_PRIVATE</b>, you can specify one of the following common values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DB_DEFAULT"></a><a id="winbio_db_default"></a><dl>
<dt><b>WINBIO_DB_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Each biometric unit in the sensor pool uses the default database specified in the default biometric unit configuration. You must specify this value if the <i>PoolType</i> parameter is <b>WINBIO_POOL_SYSTEM</b>. You cannot use this value if the <i>PoolType</i> parameter is <b>WINBIO_POOL_PRIVATE</b>

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DB_BOOTSTRAP"></a><a id="winbio_db_bootstrap"></a><dl>
<dt><b>WINBIO_DB_BOOTSTRAP</b></dt>
</dl>
</td>
<td width="60%">
You can specify this value to be used for scenarios prior to starting Windows. Typically, the database is part of the sensor chip or is part of the BIOS and can only be used for template enrollment and deletion.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DB_ONCHIP"></a><a id="winbio_db_onchip"></a><dl>
<dt><b>WINBIO_DB_ONCHIP</b></dt>
</dl>
</td>
<td width="60%">
The database is on the sensor chip and is available for enrollment and matching.

</td>
</tr>
</table>

### -param SessionHandle [out]

Pointer to the new session handle. If the function does not succeed, the handle is set to zero.

## -returns

If the function succeeds, it returns S_OK. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments have incorrect values or are incompatible with other arguments.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The session handle pointer in the <i>SessionHandle</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The <i>Flags</i> parameter contains the <b>WINBIO_FLAG_RAW</b> or the <b>WINBIO_FLAG_MAINTENANCE</b> flag and the caller has not been granted either access permission.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_UNIT</b></dt>
</dl>
</td>
<td width="60%">
One or more of the biometric unit numbers specified in the <i>UnitArray</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_NOT_ACTIVE_CONSOLE</b></dt>
</dl>
</td>
<td width="60%">
The client application is running on a remote desktop client and is attempting to open a system pool session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_SENSOR_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>PoolType</i> parameter is set to WINBIO_POOL_PRIVATE and one or more of the requested sensors in that pool is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
Current administrative policy prohibits use of the Windows Biometric Framework API.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winbio/nf-winbio-winbioclosesession">WinBioCloseSession</a>