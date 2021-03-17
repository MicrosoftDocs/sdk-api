---
UID: NF:mergemod.IMsmMerge2.ExtractFilesEx
title: IMsmMerge2::ExtractFilesEx (mergemod.h)
description: The ExtractFilesEx method extracts the embedded .cab file from a module and then writes those files to the destination directory. For more information, see the ExtractFilesEx method of the Merge object.
helpviewer_keywords: ["ExtractFilesEx","ExtractFilesEx method","ExtractFilesEx method","IMsmMerge2 interface","IMsmMerge2 interface","ExtractFilesEx method","IMsmMerge2.ExtractFilesEx","IMsmMerge2::ExtractFilesEx","_msi_extractfilesex_function","mergemod/IMsmMerge2::ExtractFilesEx","setup.imsmmerge2_extractfilesex"]
old-location: setup\imsmmerge2_extractfilesex.htm
tech.root: setup
ms.assetid: 0ba6adc9-a08f-47a6-b8a8-1624bd856511
ms.date: 12/05/2018
ms.keywords: ExtractFilesEx, ExtractFilesEx method, ExtractFilesEx method,IMsmMerge2 interface, IMsmMerge2 interface,ExtractFilesEx method, IMsmMerge2.ExtractFilesEx, IMsmMerge2::ExtractFilesEx, _msi_extractfilesex_function, mergemod/IMsmMerge2::ExtractFilesEx, setup.imsmmerge2_extractfilesex
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 2.0 or later
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mergemod.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMsmMerge2::ExtractFilesEx
 - mergemod/IMsmMerge2::ExtractFilesEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmMerge2.ExtractFilesEx
---

# IMsmMerge2::ExtractFilesEx


## -description

The 
<b>ExtractFilesEx</b> method extracts the embedded .cab file from a module and then writes those files to the destination directory. For more information, see the 
<a href="/windows/desktop/Msi/merge-extractfilesex">ExtractFilesEx</a> method of the 
<a href="/windows/desktop/Msi/merge-object">Merge</a> object.

## -parameters

### -param Path [in]

The fully qualified destination directory. A <b>LPCWSTR</b> may be used in place of a <b>BSTR</b>.

### -param fLongFileNames [in]

Set to specify using long file names for path segments and final file names.

### -param pFilePaths [out]

A pointer to a memory location. This memory location receives a second pointer to a string enumerator containing a list of fully qualified paths for the files that were extracted. The list is empty if no files can be extracted. This argument may be null. No list is provided if <i>pFilePaths</i> is Null.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_MAKE as HRESULT</b></dt>
</dl>
</td>
<td width="60%">
Could not create the output path.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OPEN_FAILED as HRESULT</b></dt>
</dl>
</td>
<td width="60%">
Could not create the output file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WRITE_FAULT as HRESULT</b></dt>
</dl>
</td>
<td width="60%">
Could not write data to the output file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unable to access embedded .cab file, or create temporary file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No embedded .cab file was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>

## -remarks

Any files in the destination directory with the same name are overwritten. The path is created if it does not already exist.

## -see-also

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>