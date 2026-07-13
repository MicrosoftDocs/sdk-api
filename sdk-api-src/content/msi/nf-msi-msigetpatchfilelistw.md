---
UID: NF:msi.MsiGetPatchFileListW
title: MsiGetPatchFileListW function (msi.h)
description: The MsiGetPatchFileList function is provided a list of .msp files, delimited by semicolons, and retrieves the list of files that can be updated by the patches. (Unicode)
helpviewer_keywords: ["MsiGetPatchFileList", "MsiGetPatchFileList function", "MsiGetPatchFileListW", "msi/MsiGetPatchFileList", "msi/MsiGetPatchFileListW", "setup.msigetpatchfilelist"]
old-location: setup\msigetpatchfilelist.htm
tech.root: setup
ms.assetid: c0a98ae4-d348-462d-8907-87116a64f79e
ms.date: 12/05/2018
ms.keywords: MsiGetPatchFileList, MsiGetPatchFileList function, MsiGetPatchFileListA, MsiGetPatchFileListW, msi/MsiGetPatchFileList, msi/MsiGetPatchFileListA, msi/MsiGetPatchFileListW, setup.msigetpatchfilelist
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista.  Windows Installer 4.5 on Windows Server 2003 and Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetPatchFileListW (Unicode) and MsiGetPatchFileListA (ANSI)
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
 - MsiGetPatchFileListW
 - msi/MsiGetPatchFileListW
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
 - MsiGetPatchFileList
 - MsiGetPatchFileListA
 - MsiGetPatchFileListW
---

# MsiGetPatchFileListW function


## -description

The <b>MsiGetPatchFileList</b> function is provided a list of .msp files, delimited by semicolons, and retrieves the list of files that can be updated by the patches.

## -parameters

### -param szProductCode [in]

A null-terminated string value containing the <a href="/windows/desktop/Msi/productcode">ProductCode</a> (GUID) of the product which is the target of the patches.  This parameter cannot be <b>NULL</b>.

### -param szPatchPackages [in]

A null-terminated string value that contains the list of Windows Installer patches (.msp files).  Each patch can be specified by the full path to the patch package. The patches in the list are delimited by semicolons. At least one patch must be specified.

### -param pcFiles [in, out]

A pointer to a location that receives the number of files that will be updated on this system by this list of patches specified by <i>szPatchList</i>. This parameter is required.

### -param pphFileRecords [in, out]

A pointer to a location that receives a pointer to an array of records. The first field (0-index) of each record  contains the full file path of a file that can be updated when the list of patches in <i>szPatchList</i> are applied on this computer. This parameter is required.

## -returns

The <b>MsiGetPatchFileList</b> function returns the following values.

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
An invalid parameter was passed to the function.

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

For example, <i>szPatchList</i> could have the value: "c:\sus\download\cache\Office\sp1.msp; c:\sus\download\cache\Office\QFE1.msp; c:\sus\download\cache\Office\QFEn.msp".

This function runs in the context of the caller. The product code is searched in the order of user-unmanaged context, user-managed context, and machine context.

You must close all MSIHANDLE objects that are returned by this function by calling 
the <a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a> function.

If the function fails, you can obtain extended error information by using the <a href="/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a> function.

For more information about using the <b>MsiGetPatchFileList</b> function  see <a href="/windows/desktop/Msi/listing-the-files-that-can-be-updated">Listing the Files that can be Updated</a>.





> [!NOTE]
> The msi.h header defines MsiGetPatchFileList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-3-1">Not Supported in Windows Installer 3.1 and earlier versions</a>
