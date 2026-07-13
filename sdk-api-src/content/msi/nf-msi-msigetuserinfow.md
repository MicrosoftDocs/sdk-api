---
UID: NF:msi.MsiGetUserInfoW
title: MsiGetUserInfoW function (msi.h)
description: The MsiGetUserInfo function returns the registered user information for an installed product. (Unicode)
helpviewer_keywords: ["MsiGetUserInfo", "MsiGetUserInfo function", "MsiGetUserInfoW", "_msi_msigetuserinfo", "msi/MsiGetUserInfo", "msi/MsiGetUserInfoW", "setup.msigetuserinfo"]
old-location: setup\msigetuserinfo.htm
tech.root: setup
ms.assetid: c05580c6-9be3-410a-aa97-be15c2980ba8
ms.date: 12/05/2018
ms.keywords: MsiGetUserInfo, MsiGetUserInfo function, MsiGetUserInfoA, MsiGetUserInfoW, _msi_msigetuserinfo, msi/MsiGetUserInfo, msi/MsiGetUserInfoA, msi/MsiGetUserInfoW, setup.msigetuserinfo
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetUserInfoW (Unicode) and MsiGetUserInfoA (ANSI)
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
 - MsiGetUserInfoW
 - msi/MsiGetUserInfoW
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
 - MsiGetUserInfo
 - MsiGetUserInfoA
 - MsiGetUserInfoW
---

# MsiGetUserInfoW function


## -description

The 
<b>MsiGetUserInfo</b> function returns the registered user information for an installed product.

## -parameters

### -param szProduct [in]

Specifies the product code for the product to be queried.

### -param lpUserNameBuf [out]

Pointer to a variable that receives the name of the user.

### -param pcchUserNameBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpUserNameBuf</i> parameter. This size should include the terminating null character.

### -param lpOrgNameBuf [out]

Pointer to a buffer that receives the organization name.

### -param pcchOrgNameBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpOrgNameBuf</i> parameter. On input, this is the full size of the buffer, including a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character.

### -param lpSerialBuf [in]

Pointer to a buffer that receives the product ID.

### -param pcchSerialBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpSerialBuf</i> parameter. On input, this is the full size of the buffer, including a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>USERINFOSTATE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
Some or all of the user information is absent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>USERINFOSTATE_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the function parameters was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>USERINFOSTATE_MOREDATA</b></dt>
</dl>
</td>
<td width="60%">
A buffer is too small to hold the requested data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>USERINFOSTATE_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>USERINFOSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The product code does not identify a known product.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

When the 
<b>MsiGetUserInfo</b> function returns, the <i>pcchNameBuf</i> parameter contains the length of the class string stored in the buffer. The count returned does not include the terminating null character. If the buffer is not big enough, the 
<b>MsiGetUserInfo</b> function returns USERINFOSTATE_MOREDATA, and 
<b>MsiGetUserInfo</b> contains the size of the string, in characters, without counting the null character.

The user information is considered to be present even in the absence of a company name.





> [!NOTE]
> The msi.h header defines MsiGetUserInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">System Status Functions</a>
