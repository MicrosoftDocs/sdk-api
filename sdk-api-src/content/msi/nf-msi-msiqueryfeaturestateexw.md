---
UID: NF:msi.MsiQueryFeatureStateExW
title: MsiQueryFeatureStateExW function (msi.h)
description: The MsiQueryFeatureStateEx function returns the installed state for a product feature. (Unicode)
helpviewer_keywords: ["INSTALLSTATE_ADVERTISED", "INSTALLSTATE_LOCAL", "INSTALLSTATE_SOURCE", "MSIINSTALLCONTEXT_MACHINE", "MSIINSTALLCONTEXT_USERMANAGED", "MSIINSTALLCONTEXT_USERUNMANAGED", "MsiQueryFeatureStateEx", "MsiQueryFeatureStateEx function", "MsiQueryFeatureStateExW", "NULL", "User SID", "msi/MsiQueryFeatureStateEx", "msi/MsiQueryFeatureStateExW", "setup.msiqueryfeaturestateex"]
old-location: setup\msiqueryfeaturestateex.htm
tech.root: setup
ms.assetid: 60165f0d-01d9-4ce8-a369-092d0c670b87
ms.date: 12/05/2018
ms.keywords: INSTALLSTATE_ADVERTISED, INSTALLSTATE_LOCAL, INSTALLSTATE_SOURCE, MSIINSTALLCONTEXT_MACHINE, MSIINSTALLCONTEXT_USERMANAGED, MSIINSTALLCONTEXT_USERUNMANAGED, MsiQueryFeatureStateEx, MsiQueryFeatureStateEx function, MsiQueryFeatureStateExA, MsiQueryFeatureStateExW, NULL, User SID, msi/MsiQueryFeatureStateEx, msi/MsiQueryFeatureStateExA, msi/MsiQueryFeatureStateExW, setup.msiqueryfeaturestateex
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiQueryFeatureStateExW (Unicode) and MsiQueryFeatureStateExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiQueryFeatureStateExW
 - msi/MsiQueryFeatureStateExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSi-Misc-L1-1-0.dll
api_name:
 - MsiQueryFeatureStateEx
 - MsiQueryFeatureStateExA
 - MsiQueryFeatureStateExW
---

# MsiQueryFeatureStateExW function


## -description

The <b>MsiQueryFeatureStateEx</b> function returns the installed state for a product feature. This function can be used to query any feature of an instance of a product installed under the machine account or any context under the current user account or the per-user-managed context under any user account other than the current user. A user must have administrative privileges to get information for a product installed for a user other than the current user.

## -parameters

### -param szProductCode [in]

<a href="/windows/desktop/Msi/productcode">ProductCode</a> GUID of the product that contains the feature of interest.

### -param szUserSid [in]

Specifies the security identifier (SID) of the account, under which, the instance of the product being queried exists. If <i>dwContext</i> is not <b>MSIINSTALLCONTEXT_MACHINE</b>,  a null value specifies the current user.

<table>
<tr>
<th>Type of SID</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NULL"></a><a id="null"></a><dl>
<dt><b>NULL</b></dt>
</dl>
</td>
<td width="60%">
NULL denotes the currently logged on user.

</td>
</tr>
<tr>
<td width="40%"><a id="User_SID"></a><a id="user_sid"></a><a id="USER_SID"></a><dl>
<dt><b>User SID</b></dt>
</dl>
</td>
<td width="60%">
Specifies enumeration for a particular user in the system.  An example of user SID is "S-1-3-64-2415071341-1358098788-3127455600-2561".

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The special SID string s-1-5-18 (system) cannot be used to enumerate features of products installed as per-machine. If <i>dwContext</i> is <b>MSIINSTALLCONTEXT_MACHINE</b>, <i>szUserSid</i> must be null.</div>
<div> </div>

### -param dwContext [in]

The installation context  of the product instance being queried.

<table>
<tr>
<th>Name</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERMANAGED"></a><a id="msiinstallcontext_usermanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERMANAGED</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the feature state for the per-user-managed instance of the product.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERUNMANAGED"></a><a id="msiinstallcontext_userunmanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERUNMANAGED</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the feature state for the per-user-unmanaged instance of the product.

<div class="alert"><b>Note</b>  When the query is made on a product installed under the per-user-unmanaged context for a user account other than the current user, the function fails.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_MACHINE"></a><a id="msiinstallcontext_machine"></a><dl>
<dt><b>MSIINSTALLCONTEXT_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the feature state for the per-machine instance of the product.

</td>
</tr>
</table>

### -param szFeature [in]

Specifies the feature being queried. Identifier of the feature as found in the <b>Feature</b> column of the <a href="/windows/desktop/Msi/feature-table">Feature table</a>.

### -param pdwState [out, optional]

Installation state of the feature for the specified product instance. This parameter can return one of the following or null.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_ADVERTISED"></a><a id="installstate_advertised"></a><dl>
<dt><b>INSTALLSTATE_ADVERTISED</b></dt>
</dl>
</td>
<td width="60%">
This feature is advertised.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_LOCAL"></a><a id="installstate_local"></a><dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The feature is installed locally.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_SOURCE"></a><a id="installstate_source"></a><dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The feature is installed to run from source.

</td>
</tr>
</table>

## -returns

The <b>MsiQueryFeatureStateEx</b> function returns the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
A user must have administrative privileges to get information for a product installed for a user other than the current user.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration data is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_FEATURE</b></dt>
</dl>
</td>
<td width="60%">
The feature ID does not identify a known feature.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The product code does not identify a known product.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected internal failure.

</td>
</tr>
</table>
 

 For more information, see 
<a href="/windows/desktop/Msi/displayed-error-messages">Displayed Error Messages</a>.

## -remarks

The 
<b>MsiQueryFeatureStateEx</b> function does not validate that the feature is actually accessible. The <b>MsiQueryFeatureStateEx</b> function does not validate the  feature ID. <b>ERROR_UNKNOWN_FEATURE</b> is returned for any unknown feature ID. When the query is made on a product installed under the per-user-unmanaged context  for a user account other than the current user, the function fails.  In this case the function returns <b>ERROR_UNKNOWN_FEATURE</b>, or if the product is advertised only  (not installed),   <b>ERROR_UNKNOWN_PRODUCT</b> is returned.





> [!NOTE]
> The msi.h header defines MsiQueryFeatureStateEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/displayed-error-messages">Displayed Error Messages</a>



<a href="/windows/desktop/Msi/feature-table">Feature Table</a>



<a href="/windows/desktop/api/msi/nf-msi-msiqueryfeaturestatea">MsiQueryFeatureState</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-2-0">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="/windows/desktop/Msi/productcode">ProductCode</a>



<a href="/windows/desktop/Msi/installer-function-reference">System Status Functions</a>
