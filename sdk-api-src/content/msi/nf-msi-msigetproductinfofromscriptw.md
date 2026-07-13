---
UID: NF:msi.MsiGetProductInfoFromScriptW
title: MsiGetProductInfoFromScriptW function (msi.h)
description: The MsiGetProductInfoFromScript function returns product information for a Windows Installer script file. (Unicode)
helpviewer_keywords: ["MsiGetProductInfoFromScript", "MsiGetProductInfoFromScript function", "MsiGetProductInfoFromScriptW", "_msi_msigetproductinfofromscript", "msi/MsiGetProductInfoFromScript", "msi/MsiGetProductInfoFromScriptW", "setup.msigetproductinfofromscript"]
old-location: setup\msigetproductinfofromscript.htm
tech.root: setup
ms.assetid: fe0bc709-b410-4a61-bea3-d11fc8f71883
ms.date: 12/05/2018
ms.keywords: MsiGetProductInfoFromScript, MsiGetProductInfoFromScript function, MsiGetProductInfoFromScriptA, MsiGetProductInfoFromScriptW, _msi_msigetproductinfofromscript, msi/MsiGetProductInfoFromScript, msi/MsiGetProductInfoFromScriptA, msi/MsiGetProductInfoFromScriptW, setup.msigetproductinfofromscript
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetProductInfoFromScriptW (Unicode) and MsiGetProductInfoFromScriptA (ANSI)
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
 - MsiGetProductInfoFromScriptW
 - msi/MsiGetProductInfoFromScriptW
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
 - MsiGetProductInfoFromScript
 - MsiGetProductInfoFromScriptA
 - MsiGetProductInfoFromScriptW
---

# MsiGetProductInfoFromScriptW function


## -description

The 
<b>MsiGetProductInfoFromScript</b> function returns product information for a Windows Installer script file.

## -parameters

### -param szScriptFile [in]

A null-terminated string specifying the full path to the script file. The script file is the advertise script that was created by calling <a href="/windows/desktop/api/msi/nf-msi-msiadvertiseproducta">MsiAdvertiseProduct</a> or <a href="/windows/desktop/api/msi/nf-msi-msiadvertiseproductexa">MsiAdvertiseProductEx</a>.

### -param lpProductBuf39 [out]

Points to a buffer that receives the product code. The buffer must be 39 characters long. The first 38 characters are for the product code 
<a href="/windows/desktop/Msi/guid">GUID</a>, and the last character is for the terminating null character.

### -param plgidLanguage [out]

Points to a variable that receives the product language.

### -param pdwVersion [out]

Points to a buffer that receives the product version.

### -param lpNameBuf [out]

Points to a buffer that receives the product name. The buffer includes a terminating null character.

### -param pcchNameBuf [in, out]

Points to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpNameBuf</i> parameter. This size should include the terminating null character. When the function returns, this variable contains the length of the string stored in the buffer. The count returned does not include the terminating null character. If the buffer is not large enough, the function returns ERROR_MORE_DATA, and the variable contains the size of the string in characters, without counting the null character.

### -param lpPackageBuf [out]

Points to a buffer that receives the package name. The buffer includes the terminating null character.

### -param pcchPackageBuf [in, out]

Points to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpPackageNameBuf</i> parameter. This size should include the terminating null character. When the function returns, this variable contains the length of the string stored in the buffer. The count returned does not include the terminating null character. If the buffer is not large enough, the function returns ERROR_MORE_DATA, and the variable contains the size of the string in characters, without counting the null character.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
A buffer was too small to hold the entire value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Could not get script information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CALL_NOT_IMPLEMENTED</b></dt>
</dl>
</td>
<td width="60%">
This function is only available on Windows 2000 and Windows XP.

</td>
</tr>
</table>

## -remarks

> [!NOTE]
> The msi.h header defines MsiGetProductInfoFromScript as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
