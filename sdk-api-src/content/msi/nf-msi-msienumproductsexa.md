---
UID: NF:msi.MsiEnumProductsExA
title: MsiEnumProductsExA function (msi.h)
description: Enumerates through one or all the instances of products that are currently advertised or installed in the specified contexts. (ANSI)
helpviewer_keywords: ["MSIINSTALLCONTEXT_MACHINE", "MSIINSTALLCONTEXT_USERMANAGED", "MSIINSTALLCONTEXT_USERUNMANAGED", "MsiEnumProductsExA", "NULL", "User SID", "msi/MsiEnumProductsExA", "s-1-1-0"]
old-location: setup\msienumproductsex.htm
tech.root: setup
ms.assetid: 33daeadc-021f-403e-808b-81a9915ae854
ms.date: 12/05/2018
ms.keywords: MSIINSTALLCONTEXT_MACHINE, MSIINSTALLCONTEXT_USERMANAGED, MSIINSTALLCONTEXT_USERUNMANAGED, MsiEnumProductsEx, MsiEnumProductsEx function, MsiEnumProductsExA, MsiEnumProductsExW, NULL, User SID, msi/MsiEnumProductsEx, msi/MsiEnumProductsExA, msi/MsiEnumProductsExW, s-1-1-0, setup.msienumproductsex
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer 3.0 or later on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiEnumProductsExW (Unicode) and MsiEnumProductsExA (ANSI)
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
 - MsiEnumProductsExA
 - msi/MsiEnumProductsExA
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
 - MsiEnumProductsEx
 - MsiEnumProductsExA
 - MsiEnumProductsExW
---

# MsiEnumProductsExA function


## -description

The <b>MsiEnumProductsEx</b> function enumerates through one or all the instances of products that are currently advertised or installed in the specified contexts. This function supersedes <a href="/windows/desktop/api/msi/nf-msi-msienumproductsa">MsiEnumProducts</a>.

## -parameters

### -param szProductCode [in, optional]

<a href="/windows/desktop/Msi/productcode">ProductCode</a> GUID of the product  to be enumerated.  Only instances of products within the scope of the context specified by the <i>szUserSid</i> and <i>dwContext</i> parameters are enumerated. This parameter can be set to <b>NULL</b> to enumerate all products in the specified context.

### -param szUserSid [in]

Null-terminated string that specifies a security identifier (SID) that restricts the context of enumeration. The special SID string s-1-1-0 (Everyone) specifies enumeration across all users in the system. A SID value other than s-1-1-0 is considered a user-SID and restricts enumeration to the current user or any user in the system. This parameter can be set to <b>NULL</b> to restrict the enumeration scope to the current user. 

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
Specifies enumeration for a particular user in the system.  An example of user SID is "S-1-3-64-2415071341-1358098788-3127455600-2561".

</td>
</tr>
<tr>
<td width="40%"><a id="s-1-1-0"></a><a id="S-1-1-0"></a><dl>
<dt><b>s-1-1-0</b></dt>
</dl>
</td>
<td width="60%">
Specifies enumeration across all users in the system.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The special SID string s-1-5-18 (System) cannot be used to enumerate products or patches installed as per-machine.  When <i>dwContext</i> is set to MSIINSTALLCONTEXT_MACHINE only, <i>szUserSid</i> must be <b>NULL</b>.</div>
<div> </div>

### -param dwContext [in]

Restricts the enumeration to a context. This parameter can be any one or a combination of the values shown in the following table.

<table>
<tr>
<th>Context</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERMANAGED"></a><a id="msiinstallcontext_usermanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERMANAGED</b></dt>
</dl>
</td>
<td width="60%">
Enumeration extended to all per–user–managed installations for the users specified by <i>szUserSid</i>. An invalid SID returns no items.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERUNMANAGED"></a><a id="msiinstallcontext_userunmanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERUNMANAGED</b></dt>
</dl>
</td>
<td width="60%">
Enumeration extended to all per–user–unmanaged installations for the users specified by <i>szUserSid</i>. An invalid SID returns no items.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_MACHINE"></a><a id="msiinstallcontext_machine"></a><dl>
<dt><b>MSIINSTALLCONTEXT_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
Enumeration extended to all per-machine installations. When <i>dwInstallContext</i> is set to MSIINSTALLCONTEXT_MACHINE only, the <i>szUserSID</i> parameter must be <b>NULL</b>.


</td>
</tr>
</table>

### -param dwIndex [in]

 Specifies the index of the product to retrieve. This parameter must be zero for the first call to the <b>MsiEnumProductsEx</b> function and then incremented for subsequent calls. The index should be incremented, only if the previous call has returned ERROR_SUCCESS. Because products are not ordered, any new product has an arbitrary index. This means that the function can return products in any order.

### -param szInstalledProductCode [out, optional]

Null-terminated string of <b>TCHAR</b> that gives the <a href="/windows/desktop/Msi/productcode">ProductCode</a> GUID of the product instance being enumerated. This parameter can be <b>NULL</b>.

### -param pdwInstalledContext [out, optional]

Returns the context of the product instance  being enumerated. The output value can be MSIINSTALLCONTEXT_USERMANAGED, MSIINSTALLCONTEXT_USERUNMANAGED, or MSIINSTALLCONTEXT_MACHINE. This parameter can be <b>NULL</b>.

### -param szSid [out, optional]

An output buffer that receives the string SID of the account under which this product instance exists.  This buffer returns an empty string for an instance installed in a per-machine context. 
 


This buffer should be large enough to contain the SID. If the buffer is too small, the function returns ERROR_MORE_DATA and sets *<i>pcchSid</i> to the number of <b>TCHAR</b> in the SID, not including the terminating NULL character.

If <i>szSid</i> is set to <b>NULL</b> and <i>pcchSid</i> is set to a valid pointer, the function returns ERROR_SUCCESS and sets *<i>pcchSid</i> to the number of <b>TCHAR</b> in the value, not including the terminating <b>NULL</b>.  The function can then be called again to retrieve the value, with the  <i>szSid</i> buffer large enough to contain *<i>pcchSid</i> + 1 characters.

If <i>szSid</i> and <i>pcchSid</i> are both set to <b>NULL</b>, the function returns ERROR_SUCCESS if the value exists, without  retrieving the value.

### -param pcchSid [in, out, optional]

When calling the function, this parameter should be a pointer to a variable that specifies the number of <b>TCHAR</b> in the <i>szSid</i> buffer. When the function returns, this parameter is set to the size of the requested value whether or not the function copies the value into the specified buffer. The size is returned as the number of <b>TCHAR</b> in the requested value, not including the terminating null character. 

This parameter can be set to <b>NULL</b> only if <i>szSid</i> is also <b>NULL</b>, otherwise the function returns ERROR_INVALID_PARAMETER.

## -returns

The <b>MsiEnumProductsEx</b> function returns one of the following values.

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
If the scope includes users other than the current user, you need administrator privileges. 

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
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more products to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
A product is enumerated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>szSid</i> parameter is too small to get the user SID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The product is not installed on the computer in the specified context.

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

## -remarks

To enumerate products, an application must initially call the <b>MsiEnumProductsEx</b> function with the <i>iIndex</i> parameter set to zero. The application must then increment the <i>iProductIndex</i> parameter and call <b>MsiEnumProductsEx</b> until it returns <b>ERROR_NO_MORE_ITEMS</b> and there are no more products to enumerate.

When making multiple calls to <b>MsiEnumProductsEx</b> to enumerate all of the products, each call must be made from the same thread.

A user must have administrator privileges to enumerate products across all user accounts or a user account other than the current user account. The enumeration skips products that are advertised only (such as products  not installed) in the per-user-unmanaged context when enumerating across all users or a user other than the current user.

Use <a href="/windows/desktop/api/msi/nf-msi-msigetproductinfoexa">MsiGetProductInfoEx</a> to get the state or other information about each product instance enumerated by <b>MsiEnumProductsEx</b>.





> [!NOTE]
> The msi.h header defines MsiEnumProductsEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/msi/nf-msi-msienumproductsa">MsiEnumProducts</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-2-0">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="/windows/desktop/Msi/productcode">ProductCode</a>



<a href="/windows/desktop/Msi/removing-patches">Removing Patches</a>
