---
UID: NF:msi.MsiExtractPatchXMLDataW
title: MsiExtractPatchXMLDataW function (msi.h)
description: The MsiExtractPatchXMLData function extracts information from a patch that can be used to determine if the patch applies to a target system. (Unicode)
helpviewer_keywords: ["MsiExtractPatchXMLData", "MsiExtractPatchXMLData function", "MsiExtractPatchXMLDataW", "msi/MsiExtractPatchXMLData", "msi/MsiExtractPatchXMLDataW", "setup.msiextractpatchxmldata"]
old-location: setup\msiextractpatchxmldata.htm
tech.root: setup
ms.assetid: b0044783-552d-4492-bb1d-337227dd3e16
ms.date: 12/05/2018
ms.keywords: MsiExtractPatchXMLData, MsiExtractPatchXMLData function, MsiExtractPatchXMLDataA, MsiExtractPatchXMLDataW, msi/MsiExtractPatchXMLData, msi/MsiExtractPatchXMLDataA, msi/MsiExtractPatchXMLDataW, setup.msiextractpatchxmldata
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer 3.0 or later on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiExtractPatchXMLDataW (Unicode) and MsiExtractPatchXMLDataA (ANSI)
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
 - MsiExtractPatchXMLDataW
 - msi/MsiExtractPatchXMLDataW
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
 - MsiExtractPatchXMLData
 - MsiExtractPatchXMLDataA
 - MsiExtractPatchXMLDataW
---

# MsiExtractPatchXMLDataW function


## -description

The <b>MsiExtractPatchXMLData</b> function extracts information from a patch  that can be used to determine if the patch applies to a target system. The function returns an XML string that can be provided to <a href="/windows/desktop/api/msi/nf-msi-msideterminepatchsequencea">MsiDeterminePatchSequence</a> and <a href="/windows/desktop/api/msi/nf-msi-msidetermineapplicablepatchesa">MsiDetermineApplicablePatches</a> instead of the full patch file. The returned information  can be used to determine whether the patch is applicable.

## -parameters

### -param szPatchPath [in]

The  full path to the patch that is being queried. Pass in as a null-terminated string. This parameter cannot be <b>NULL</b>.

### -param dwReserved [in]

A reserved argument that must be 0 (zero).

### -param szXMLData [out, optional]

A pointer to a buffer to hold the XML string that contains the extracted patch information. This buffer should be large enough to contain the received information. If the buffer is too small, the function returns ERROR_MORE_DATA and sets *<i>pcchXMLData</i> to the number of <b>TCHAR</b> in the value, not including the terminating NULL character.



If <i>szXMLData</i> is set to <b>NULL</b> and <i>pcchXMLData</i> is set to a valid pointer,  the function returns ERROR_SUCCESS and sets *<i>pcchXMLData</i> to the number of <b>TCHAR</b> in the value, not including the terminating NULL character.  The function can then be called again to retrieve the value, with <i>szXMLData</i> buffer large enough to contain *<i>pcchXMLData</i> + 1 characters.

### -param pcchXMLData [in, out, optional]

A pointer to a variable that specifies the number of <b>TCHAR</b> in the <i>szXMLData</i> buffer. When the function returns, this parameter is set to the size of the requested value whether or not the function copies the value into the specified buffer. The size is returned as the number of <b>TCHAR</b> in the requested value, not including the terminating null character.

If this parameter is set to <b>NULL</b>, the function returns ERROR_INVALID_PARAMETER.

## -returns

The <b>MsiExtractPatchXMLData</b> function can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The function failed in a way that is not identified by any of the return values in this table.

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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The value does not fit in the provided buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATCH_OPEN_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The patch file could not be opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATCH_PACKAGE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The patch file could not be opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CALL_NOT_IMPLEMENTED</b></dt>
</dl>
</td>
<td width="60%">
This error can be returned  if MSXML 3.0 is not installed. 

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/Msi/installer-extractpatchxmldata">ExtractPatchXMLData</a> method of the <a href="/windows/desktop/Msi/installer-object">Installer</a> object uses the <b>MsiExtractPatchXMLData</b> function.





> [!NOTE]
> The msi.h header defines MsiExtractPatchXMLData as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/msi/nf-msi-msidetermineapplicablepatchesa">MsiDetermineApplicablePatches </a>



<a href="/windows/desktop/api/msi/nf-msi-msideterminepatchsequencea">MsiDeterminePatchSequence</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-2-0">Not Supported in Windows Installer 2.0 and earlier</a>
