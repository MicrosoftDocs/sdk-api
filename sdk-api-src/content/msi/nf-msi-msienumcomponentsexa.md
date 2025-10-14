---
UID: NF:msi.MsiEnumComponentsExA
title: MsiEnumComponentsExA function (msi.h)
description: The MsiEnumComponentsEx function enumerates installed components. The function retrieves the component code for one component each time it is called. The component code is the string GUID unique to the component, version, and language. (ANSI)
helpviewer_keywords: ["MSIINSTALLCONTEXT_MACHINE", "MSIINSTALLCONTEXT_USERMANAGED", "MSIINSTALLCONTEXT_USERUNMANAGED", "MsiEnumComponentsExA", "NULL", "User SID", "msi/MsiEnumComponentsExA", "s-1-1-0"]
old-location: setup\msienumcomponentsex.htm
tech.root: setup
ms.assetid: c804cd64-7bb5-4dd1-aca2-94455cc99a15
ms.date: 12/05/2018
ms.keywords: MSIINSTALLCONTEXT_MACHINE, MSIINSTALLCONTEXT_USERMANAGED, MSIINSTALLCONTEXT_USERUNMANAGED, MsiEnumComponentsEx, MsiEnumComponentsEx function [Setup API], MsiEnumComponentsExA, MsiEnumComponentsExW, NULL, User SID, msi/MsiEnumComponentsEx, msi/MsiEnumComponentsExA, msi/MsiEnumComponentsExW, s-1-1-0, setup.msienumcomponentsex
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiEnumComponentsExW (Unicode) and MsiEnumComponentsExA (ANSI)
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
 - MsiEnumComponentsExA
 - msi/MsiEnumComponentsExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiEnumComponentsEx
 - MsiEnumComponentsExA
 - MsiEnumComponentsExW
---

# MsiEnumComponentsExA function


## -description

The <b>MsiEnumComponentsEx</b> function enumerates installed components. The function retrieves the component code for one component each time it is called. The component code is the string GUID unique to the component, version, and language. 


<b><a href="/windows/desktop/Msi/not-supported-in-windows-installer-4-5">Windows Installer 4.5 or earlier</a>:  </b>Not supported. This function is available beginning with Windows Installer 5.0.

## -parameters

### -param szUserSid [in, optional]

A null-terminated string that contains a security identifier (SID.) The enumeration of installed components extends to users identified by this SID. The special SID string s-1-1-0 (Everyone) specifies an enumeration of all installed components across all products of all users in the system. A SID value other than s-1-1-0 specifies a user SID for a particular user and restricts the enumeration to instances of  applications installed by the specified user.

<table>
<tr>
<th>SID type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NULL"></a><a id="null"></a><dl>
<dt><b>NULL</b></dt>
</dl>
</td>
<td width="60%">
Specifies the currently logged-on user.

</td>
</tr>
<tr>
<td width="40%"><a id="User_SID"></a><a id="user_sid"></a><a id="USER_SID"></a><dl>
<dt><b>User SID</b></dt>
</dl>
</td>
<td width="60%">
An enumeration for a specific user in the system. An example of an user SID is "S-1-3-64-2415071341-1358098788-3127455600-2561".

</td>
</tr>
<tr>
<td width="40%"><a id="s-1-1-0"></a><a id="S-1-1-0"></a><dl>
<dt><b>s-1-1-0</b></dt>
</dl>
</td>
<td width="60%">
Specifies all users in the system.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  <p class="note">The special SID string s-1-5-18 (System) cannot be used to enumerate applications installed in the per-machine installation context.  Setting the SID value to s-1-5-18 returns ERROR_INVALID_PARAMETER. When <i>dwContext</i> is set to MSIINSTALLCONTEXT_MACHINE only, <i>szUserSid</i> must be <b>NULL</b>. 


</div>
<div> </div>

### -param dwContext [in]

A flag that restricts the enumeration of  installed component to instances of products installed in the specified installation context. The enumeration includes only product instances installed by the users specified by  <i>szUserSid</i>. 

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERMANAGED"></a><a id="msiinstallcontext_usermanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERMANAGED</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Include products that exist in  the per–user–managed installation context. 

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERUNMANAGED"></a><a id="msiinstallcontext_userunmanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERUNMANAGED</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Include products that exist in  the per–user–unmanaged installation context.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_MACHINE"></a><a id="msiinstallcontext_machine"></a><dl>
<dt><b>MSIINSTALLCONTEXT_MACHINE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Include products that exist in the per-machine installation context. When <i>dwInstallContext</i> is set to MSIINSTALLCONTEXT_MACHINE only, the <i>szUserSID</i> parameter must be <b>NULL</b>.


</td>
</tr>
</table>

### -param dwIndex [in]

Specifies the index of the component to retrieve.  This parameter must be zero (0) for the first call to <b>MsiEnumComponentsEx</b> function.  For each subsequent call, the index must be incremented by 1.  The index should only be incremented if the previous call to the function returns ERROR_SUCCESS.
Components are not ordered and can be returned by the function in any order.

### -param szInstalledComponentCode [out, optional]

An output buffer that receives the component code GUID for the installed component. The length of the buffer should be large enough to hold a  null-terminated string value containing the component code. The first 38 <b>TCHAR</b> characters receives the GUID for the component, and the 39th character receives a terminating  NULL character.

### -param pdwInstalledContext [out, optional]

A flag that gives the installation context the application that installed the component.


<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERMANAGED"></a><a id="msiinstallcontext_usermanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERMANAGED</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The application is installed in the per–user–managed installation context. 

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERUNMANAGED"></a><a id="msiinstallcontext_userunmanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERUNMANAGED</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The application is installed in the per–user–unmanaged installation context.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_MACHINE"></a><a id="msiinstallcontext_machine"></a><dl>
<dt><b>MSIINSTALLCONTEXT_MACHINE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The application is installed  in the per-machine installation installation context. 

</td>
</tr>
</table>

### -param szSid [out, optional]

Receives the security identifier (SID) that identifies the user that installed the application that owns the component. The location receives an empty string if this instance of the application is installed in a per-machine installation context. 

The length of the buffer at this location should be large enough to hold a null-terminated string  value containing the SID. If the buffer is too small, the function returns <b>ERROR_MORE_DATA</b> and the location pointed to by <i>pcchSid</i> receives  the number of <b>TCHAR</b> in the SID, not including the terminating NULL character.

If <i>szSid</i> is set to <b>NULL</b> and <i>pcchSid</i> is a valid pointer to a location in memory, the function returns <b>ERROR_SUCCESS</b> and the location receives the number of <b>TCHAR</b> in the SID, not including the terminating null character. The function can then be called again to retrieve the value, with the <i>szSid</i> buffer resized large enough to contain *pcchSid + 1 characters.



<table>
<tr>
<th>SID type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>Empty string</dt>
</dl>
</td>
<td width="60%">
The application is installed in a per-machine installation context.

</td>
</tr>
<tr>
<td width="40%"><a id="User_SID"></a><a id="user_sid"></a><a id="USER_SID"></a><dl>
<dt><b>User SID</b></dt>
</dl>
</td>
<td width="60%">
The SID for the user in the system that installed the application. 

</td>
</tr>
</table>

### -param pcchSid [in, out]

Receives the number of <b>TCHAR</b> in the SID, not including the terminating null character. When the function returns, this variable is set to the size of the requested SID whether or not the function can successfully copy the SID and terminating null character into the buffer location pointed to by <i>szSid</i>. The size is returned as the number of <b>TCHAR</b> in the requested value, not including the terminating null character. 



This parameter can be set to <b>NULL</b> only if <i>szSid</i> is also <b>NULL</b>, otherwise the function returns <b>ERROR_INVALID_PARAMETER</b>. If <i>szSid</i> and <i>pcchSid</i> are both set to <b>NULL</b>, the function returns <b>ERROR_SUCCESS</b> if the SID exists, without retrieving the SID value.

## -returns

The <a href="/windows/desktop/api/msi/nf-msi-msienumproductsexa">MsiEnumProductsEx</a> function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Administrator privileges are required to enumerate components of applications installed by users other than the current user. 

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
An invalid parameter is passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more components to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The provided buffer was too small to hold the entire value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The function failed.

</td>
</tr>
</table>

## -remarks

> [!NOTE]
> The msi.h header defines MsiEnumComponentsEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
