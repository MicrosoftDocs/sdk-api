---
UID: NF:setupapi.SetupCopyOEMInfA
title: SetupCopyOEMInfA function (setupapi.h)
description: The SetupCopyOEMInf function copies a specified .inf file to the %windir%/Inf directory. (ANSI)
helpviewer_keywords: ["SPOST_NONE", "SPOST_PATH", "SPOST_URL", "SP_COPY_DELETESOURCE", "SP_COPY_NOOVERWRITE", "SP_COPY_OEMINF_CATALOG_ONLY", "SP_COPY_REPLACEONLY", "SetupCopyOEMInfA", "setupapi/SetupCopyOEMInfA"]
old-location: setup\setupcopyoeminf.htm
tech.root: setup
ms.assetid: f082145d-b3e7-4efd-8820-3376a36f3710
ms.date: 12/05/2018
ms.keywords: SPOST_NONE, SPOST_PATH, SPOST_URL, SP_COPY_DELETESOURCE, SP_COPY_NOOVERWRITE, SP_COPY_OEMINF_CATALOG_ONLY, SP_COPY_REPLACEONLY, SetupCopyOEMInf, SetupCopyOEMInf function [Setup API], SetupCopyOEMInfA, SetupCopyOEMInfW, _setupapi_setupcopyoeminf, setup.setupcopyoeminf, setupapi/SetupCopyOEMInf, setupapi/SetupCopyOEMInfA, setupapi/SetupCopyOEMInfW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupCopyOEMInfW (Unicode) and SetupCopyOEMInfA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupCopyOEMInfA
 - setupapi/SetupCopyOEMInfA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupCopyOEMInf
 - SetupCopyOEMInfA
 - SetupCopyOEMInfW
req.apiset: ext-ms-win-setupapi-classinstallers-l1-1-2 (introduced in Windows 10, version 10.0.14393)
---

# SetupCopyOEMInfA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The <b>SetupCopyOEMInf</b> function copies a specified .inf file to the %windir%/Inf directory.

A caller of this function is required have administrative privileges, otherwise the function fails.

## -parameters

### -param SourceInfFileName [in]

Full path to the source .inf file. You should use a null-terminated string. This path should not exceed <b>MAX_PATH</b> in size, including the terminating <b>NULL</b>.

### -param OEMSourceMediaLocation [in]

Source location information to be stored in the precompiled .inf (.pnf). This location information is specific to the source media type specified. You should use a null-terminated string. This path should not exceed <b>MAX_PATH</b> in size, including the terminating <b>NULL</b>.

### -param OEMSourceMediaType [in]

Source media type referenced by the location information. This parameter may be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPOST_NONE"></a><a id="spost_none"></a><dl>
<dt><b>SPOST_NONE</b></dt>
</dl>
</td>
<td width="60%">
No source media information is stored in the .pnf file. The value of <i>OEMSourceMediaLocation</i> is ignored in this case.

</td>
</tr>
<tr>
<td width="40%"><a id="SPOST_PATH"></a><a id="spost_path"></a><dl>
<dt><b>SPOST_PATH</b></dt>
</dl>
</td>
<td width="60%">
<i>OEMSourceMediaLocation</i> contains a path to the source media. For example, if the media is on a floppy, this path might be "A:\". If <i>OEMSourceMediaLocation</i> is <b>NULL</b>, the path is assumed to be the path where the .inf is located. If the .inf has a corresponding .pnf in that location, the .pnf file's source media information is transferred to the destination .pnf file.

</td>
</tr>
<tr>
<td width="40%"><a id="SPOST_URL"></a><a id="spost_url"></a><dl>
<dt><b>SPOST_URL</b></dt>
</dl>
</td>
<td width="60%">
<i>OEMSourceMediaLocation</i> contains a universal resource locator (URL) that specifies the Internet location from where the .inf/driver files were retrieved. If <i>OEMSourceMediaLocation</i> is <b>NULL</b>, it is assumed that the default Code Download Manager location was used.

</td>
</tr>
</table>

### -param CopyStyle [in]

Specifies how the .inf file is copied into the .inf directory. The following flags can be combined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_DELETESOURCE"></a><a id="sp_copy_deletesource"></a><dl>
<dt><b>SP_COPY_DELETESOURCE</b></dt>
</dl>
</td>
<td width="60%">
Delete source file on successful copy.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_REPLACEONLY"></a><a id="sp_copy_replaceonly"></a><dl>
<dt><b>SP_COPY_REPLACEONLY</b></dt>
</dl>
</td>
<td width="60%">
Copy only if this file already exists in the Inf directory. This flag could be used to update the source location information for an existing .inf.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_NOOVERWRITE"></a><a id="sp_copy_nooverwrite"></a><dl>
<dt><b>SP_COPY_NOOVERWRITE</b></dt>
</dl>
</td>
<td width="60%">
Copy only if the specified files do not currently exist in the Inf directory. If the .inf does currently exist, this API fails and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_FILE_EXISTS. In this case, the existing .inf file's filename is placed into the appropriate field in the destination .inf file's information output buffers.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_OEMINF_CATALOG_ONLY"></a><a id="sp_copy_oeminf_catalog_only"></a><dl>
<dt><b>SP_COPY_OEMINF_CATALOG_ONLY</b></dt>
</dl>
</td>
<td width="60%">
The specified .inf file's corresponding catalog files is copied to %windir%\Inf. If this flag is specified, the destination filename information is entered upon successful return if the specified .inf file already exists in the Inf directory.

</td>
</tr>
</table>

### -param DestinationInfFileName [out, optional]

Pointer to a buffer to receive the .inf file name assigned to it at the time it was copied to the Inf directory. The buffer, if specified, should typically be <b>MAX_PATH</b> in length. If the SP_COPY_NOOVERWRITE flag is specified and the <b>SetupCopyOEMInf</b> function fails with a return code of ERROR_FILE_EXISTS, this buffer contains the name of the existing .inf file. If the SP_COPY_OEMINF_CATALOG_ONLY flag is specified, this buffer contains the destination .inf filename if the .inf file is already present in the Inf directory. Otherwise, this buffer is set to the empty string. This parameter can be <b>NULL</b>.

### -param DestinationInfFileNameSize [in]

Size of the <i>DestinationInfFileName</i> buffer, in characters, or zero if the buffer is not specified. If <i>DestinationInfFileName</i> is specified and this buffer size is less than the size required to return the destination .inf filename (including full path), this function fails. In this case <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER.

### -param RequiredSize [out, optional]

Pointer to a variable that receives the size (in characters) required to store the destination .inf file name including a terminating <b>NULL</b>. If the SP_COPY_OEMINF_CATALOG_ONLY flag is specified, this variable receives a string length only if the .inf file already exists in the Inf directory. Otherwise, this variable is set to zero. This parameter can be <b>NULL</b>.

### -param DestinationInfFileNameComponent [out, optional]

Pointer to a string that is set upon successful return (or ERROR_FILE_EXISTS) to point to the beginning of the filename component of the path stored in the <i>DestinationInfFileName</i> parameter. If the SP_COPY_OEMINF_CATALOG_ONLY flag is specified, the <i>DestinationInfFileName</i> parameter may be an empty string. In this case, the character pointer is set to <b>NULL</b> upon successful return. This parameter can be <b>NULL</b>.

## -returns

This function returns WINSETUPAPI BOOL.

## -remarks

The 
<b>SetupCopyOEMInf</b> function copies a specified .inf file into the %windir%\Inf directory. 
<b>SetupCopyOEMInf</b> does not recopy the file if it finds that a binary image of the specified .inf file already exists in the Inf directory with the same name or a name of the form OEM*.inf. When 
<b>SetupCopyOEMInf</b> copies a file, it renames the copied file to OEM*.inf. Name provided is unique and cannot be predicted.

<b>SetupCopyOEMInf</b> uses the following procedure to determine if the .inf file already exists in the Inf directory:

All .inf files with names of the form OEM*.inf are enumerated and any files that have the same file size as the specified .inf file are binary compared.

The Inf directory is searched for the source filename of the .inf file. If an .inf file of the same name exists and is the same size as that of the specified .inf file, the two files are binary compared to determine if they are identical.

If the specified .inf file already exists a further check is performed to determine if the specified .inf file contains a CatalogFile= entry in its [Version] section. If it does, the .inf file's %windir%\Inf primary filename with a ".cat" extension is used to determine if the catalog is already installed. If there is a catalog installed, but it is not the same as the catalog associated with the source .inf, this is not considered to be a match and enumerations continue. It is possible to have multiple identical .inf files with unique catalogs contained in %windir%\Inf directory. If an existing match is not found, the .inf and .cat files are installed under a new and unique name.

OEM .inf files that do not specify a CatalogFile= entry are considered invalid with respect to digital signature verification.

In cases where the .inf file must be copied to the %windir%\Inf directory, any digital signature verification failures are reported.

If the .inf and .cat files already exist, these existing filenames are used and the file replacement behavior is based on the specified CopyStyle flags. Replacement behavior refers only to the source media information stored in the .pnf. Existing .inf, .pnf, and .cat files are not modified.





> [!NOTE]
> The setupapi.h header defines SetupCopyOEMInf as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupuninstalloeminfa">SetupUninstallOEMInf</a>
