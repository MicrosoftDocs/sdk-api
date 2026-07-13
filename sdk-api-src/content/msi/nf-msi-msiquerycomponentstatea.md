---
UID: NF:msi.MsiQueryComponentStateA
title: MsiQueryComponentStateA function (msi.h)
description: The MsiQueryComponentState function returns the installed state for a component. (ANSI)
helpviewer_keywords: ["INSTALLSTATE_LOCAL", "INSTALLSTATE_SOURCE", "MSIINSTALLCONTEXT_MACHINE", "MSIINSTALLCONTEXT_USERMANAGED", "MSIINSTALLCONTEXT_USERUNMANAGED", "MsiQueryComponentStateA", "NULL", "User SID", "msi/MsiQueryComponentStateA"]
old-location: setup\msiquerycomponentstate.htm
tech.root: setup
ms.assetid: d3b387d1-720e-4b54-ba80-731fcabdf676
ms.date: 12/05/2018
ms.keywords: INSTALLSTATE_LOCAL, INSTALLSTATE_SOURCE, MSIINSTALLCONTEXT_MACHINE, MSIINSTALLCONTEXT_USERMANAGED, MSIINSTALLCONTEXT_USERUNMANAGED, MsiQueryComponentState, MsiQueryComponentState function, MsiQueryComponentStateA, MsiQueryComponentStateW, NULL, User SID, msi/MsiQueryComponentState, msi/MsiQueryComponentStateA, msi/MsiQueryComponentStateW, setup.msiquerycomponentstate
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiQueryComponentStateW (Unicode) and MsiQueryComponentStateA (ANSI)
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
 - MsiQueryComponentStateA
 - msi/MsiQueryComponentStateA
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
 - MsiQueryComponentState
 - MsiQueryComponentStateA
 - MsiQueryComponentStateW
---

# MsiQueryComponentStateA function


## -description

The <b>MsiQueryComponentState</b> function returns the installed state for a component. This function can query for a component of an instance of a product that is installed under user accounts other than the  current user provided the product is not advertised under the per-user-unmanaged context for a user account other than the current user.  The calling process must have administrative privileges to get information for a product installed for a user other than the current user.

## -parameters

### -param szProductCode [in]

Specifies the <a href="/windows/desktop/Msi/productcode">ProductCode</a> GUID for the product that contains the component.

### -param szUserSid [in]

Specifies the security identifier (SID) of the account under which the instance of the product being queried exists. If <i>dwContext</i> is not MSIINSTALLCONTEXT_MACHINE, null specifies the current user.

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
 

<div class="alert"><b>Note</b>  The special SID string "S-1-5-18" (system) cannot be used to enumerate products installed as per-machine. If <i>dwContext</i> is <b>MSIINSTALLCONTEXT_MACHINE</b>, <i>szUserSid</i> must be null.</div>
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
Retrieves the component's state for the per–user–managed instance of the product.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERUNMANAGED"></a><a id="msiinstallcontext_userunmanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERUNMANAGED</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the component's state for the per–user–non-managed instance of the product.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_MACHINE"></a><a id="msiinstallcontext_machine"></a><dl>
<dt><b>MSIINSTALLCONTEXT_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the component's state for the per-machine instance of the product.

</td>
</tr>
</table>

### -param szComponentCode [in]

Specifies the component being queried. Component code GUID of the component as found in the ComponentID column of the <a href="/windows/desktop/Msi/component-table">Component</a> table.

### -param pdwState [out]

Installation state of the component for the specified product instance. This parameter can return one of the following or null values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_LOCAL"></a><a id="installstate_local"></a><dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The component is installed locally.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_SOURCE"></a><a id="installstate_source"></a><dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The component is installed to run from the source.

</td>
</tr>
</table>

## -returns

The <b>MsiQueryComponentState</b> function returns the following values.

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
The calling process must have administrative privileges to get information for a product installed for a user other than the current user.

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
<dt><b>ERROR_UNKNOWN_COMPONENT</b></dt>
</dl>
</td>
<td width="60%">
The component ID does not identify a known component.

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
Failures that cannot be ascribed to any Windows error code.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
Buffer too small to get the user SID.

</td>
</tr>
</table>
 

For more information, see 
<a href="/windows/desktop/Msi/displayed-error-messages">Displayed Error Messages</a>.

## -see-also

<a href="/windows/desktop/Msi/component-table">Component</a>



<a href="/windows/desktop/Msi/displayed-error-messages">Displayed Error Messages</a>



<a href="/windows/desktop/Msi/database-functions">Installer Selection Functions</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-2-0">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="/windows/desktop/Msi/productcode">ProductCode</a>

## -remarks

> [!NOTE]
> The msi.h header defines MsiQueryComponentState as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
