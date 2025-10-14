---
UID: NF:msi.MsiEnumClientsExW
title: MsiEnumClientsExW function (msi.h)
description: The MsiEnumClientsEx function enumerates the installed applications that use a specified component. The function retrieves a product code for an application each time it is called. (Unicode)
helpviewer_keywords: ["MSIINSTALLCONTEXT_MACHINE", "MSIINSTALLCONTEXT_USERMANAGED", "MSIINSTALLCONTEXT_USERUNMANAGED", "MsiEnumClientsEx", "MsiEnumClientsEx function [Setup API]", "MsiEnumClientsExW", "NULL", "User SID", "msi/MsiEnumClientsEx", "msi/MsiEnumClientsExW", "s-1-1-0", "setup.msienumclientsex"]
old-location: setup\msienumclientsex.htm
tech.root: setup
ms.assetid: f7677202-1b3d-4039-86d3-242c3ce984e4
ms.date: 12/05/2018
ms.keywords: MSIINSTALLCONTEXT_MACHINE, MSIINSTALLCONTEXT_USERMANAGED, MSIINSTALLCONTEXT_USERUNMANAGED, MsiEnumClientsEx, MsiEnumClientsEx function [Setup API], MsiEnumClientsExA, MsiEnumClientsExW, NULL, User SID, msi/MsiEnumClientsEx, msi/MsiEnumClientsExA, msi/MsiEnumClientsExW, s-1-1-0, setup.msienumclientsex
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiEnumClientsExW (Unicode) and MsiEnumClientsExA (ANSI)
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
 - MsiEnumClientsExW
 - msi/MsiEnumClientsExW
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
 - MsiEnumClientsEx
 - MsiEnumClientsExA
 - MsiEnumClientsExW
---

# MsiEnumClientsExW function


## -description

The 
<b>MsiEnumClientsEx</b> function enumerates the installed applications that use a specified component. The function retrieves a  <a href="/windows/desktop/Msi/product-codes">product code</a> for an application each time it is called.


<b><a href="/windows/desktop/Msi/not-supported-in-windows-installer-4-5">Windows Installer 4.5 or earlier</a>:  </b>Not supported. This function is available beginning with Windows Installer 5.0.

## -parameters

### -param szComponent [in]

The component code GUID that identifies the component. The function enumerates the applications that use this component.

### -param szUserSid [in, optional]

A null-terminated string value that contains a security identifier (SID.) The enumeration of applications extends to users identified by this SID. The special SID string s-1-1-0 (Everyone) enumerates all applications for all users in the system. A SID value other than s-1-1-0 specifies a user SID for a particular user and enumerates the instances of  applications installed by the specified user.

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
Specifies an enumeration for a particular user. An example of an user SID is "S-1-3-64-2415071341-1358098788-3127455600-2561".

</td>
</tr>
<tr>
<td width="40%"><a id="s-1-1-0"></a><a id="S-1-1-0"></a><dl>
<dt><b>s-1-1-0</b></dt>
</dl>
</td>
<td width="60%">
Specifies an enumeration for all users in the system.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The special SID string s-1-5-18 (System) cannot be used to enumerate applications that exist in the per-machine installation context.  Setting the SID value to s-1-5-18 returns <b>ERROR_INVALID_PARAMETER</b>. When <i>dwContext</i> is set to <b>MSIINSTALLCONTEXT_MACHINE</b> only, the value of <i>szUserSid</i> must be <b>NULL</b>. 
</div>
<div> </div>

### -param dwContext [in]

A flag that extends the enumeration to instances of applications installed in the specified installation context. The enumeration includes only instances of applications that are installed by the users identified by  <i>szUserSid</i>. 


This can be a combination of the following values.



<table>
<tr>
<th>Context</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERMANAGED"></a><a id="msiinstallcontext_usermanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERMANAGED</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Include applications installed in  the per–user–managed installation context. 

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERUNMANAGED"></a><a id="msiinstallcontext_userunmanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERUNMANAGED</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Include applications installed in  the per–user–unmanaged installation context.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_MACHINE"></a><a id="msiinstallcontext_machine"></a><dl>
<dt><b>MSIINSTALLCONTEXT_MACHINE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Include applications installed in the per-machine installation context. When <i>dwInstallContext</i> is set to <b>MSIINSTALLCONTEXT_MACHINE</b> only, the value of the <i>szUserSID</i> parameter must be <b>NULL</b>.


</td>
</tr>
</table>

### -param dwProductIndex [in]

Specifies the index of the application to retrieve.  The value of this parameter must be zero (0) in the first call to the function.  For each subsequent call, the index must be incremented by 1.  The index should only be incremented if the previous call to the function returns <b>ERROR_SUCCESS</b>.

### -param szProductBuf [out, optional]

A string value that receives the product code for the application. The length of the buffer at this location should be large enough to hold a  null-terminated string value containing the product code. The first 38 <b>TCHAR</b> characters receives the GUID for the component, and the 39th character receives a terminating  NULL character.

### -param pdwInstalledContext [out, optional]

A flag that gives the installation context of the application.


This can be a combination of the following values.



<table>
<tr>
<th>Context</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERMANAGED"></a><a id="msiinstallcontext_usermanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERMANAGED</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The application is installed  in the per–user–managed installation context. 

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERUNMANAGED"></a><a id="msiinstallcontext_userunmanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERUNMANAGED</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The application is installed  in the per–user–unmanaged installation context.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_MACHINE"></a><a id="msiinstallcontext_machine"></a><dl>
<dt><b>MSIINSTALLCONTEXT_MACHINE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The application is in the per-machine installation installation context. 

</td>
</tr>
</table>

### -param szSid [out, optional]

Receives the security identifier (SID) that identifies the user that installed the application. The location receives an empty string value if this instance of the application exists in a per-machine installation context. 

The length of the buffer should be large enough to hold a null-terminated string  value containing the SID. If the buffer is too small, the function returns <b>ERROR_MORE_DATA</b> and the location pointed to by <i>pcchSid</i> receives  the number of <b>TCHAR</b> in the SID, not including the terminating NULL character.

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
The SID for the user that installed the product. 

</td>
</tr>
</table>

### -param pcchSid [in, out, optional]

Pointer to a location in memory that contains a variable that specifies the number of <b>TCHAR</b> in the SID, not including the terminating null character. When the function returns, this variable is set to the size of the requested SID whether or not the function can successfully copy the SID and terminating null character into the buffer location pointed to by <i>szSid</i>. The size is returned as the number of TCHAR in the requested value, not including the terminating null character. 



This parameter can be set to <b>NULL</b> only if <i>szSid</i> is also <b>NULL</b>, otherwise the function returns <b>ERROR_INVALID_PARAMETER</b>. If <i>szSid</i> and <i>pcchSid</i> are both set to <b>NULL</b>, the function returns <b>ERROR_SUCCESS</b> if the SID exists, without retrieving the SID value.

## -returns

The <b>MsiEnumClientsEx</b> function returns one of the following values.

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
Administratator privileges are required to enumerate components of applications installed by users other than the current user. 

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
There are no more applications to enumerate.

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
> The msi.h header defines MsiEnumClientsEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
