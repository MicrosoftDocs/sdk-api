---
UID: NF:mergemod.IMsmMerge.ExtractFiles
title: IMsmMerge::ExtractFiles (mergemod.h)
description: The ExtractFiles method extracts the embedded .cab file from a module and then writes those files to the destination directory. For more information, see the ExtractFiles method of the Merge object.
helpviewer_keywords: ["ExtractFiles","ExtractFiles method","ExtractFiles method","IMsmMerge interface","IMsmMerge interface","ExtractFiles method","IMsmMerge.ExtractFiles","IMsmMerge::ExtractFiles","_msi_extractfiles_function","mergemod/IMsmMerge::ExtractFiles","setup.imsmmerge_extractfiles"]
old-location: setup\imsmmerge_extractfiles.htm
tech.root: setup
ms.assetid: e5bafd2d-0750-4aa6-87e8-22ef3cfdd5ff
ms.date: 12/05/2018
ms.keywords: ExtractFiles, ExtractFiles method, ExtractFiles method,IMsmMerge interface, IMsmMerge interface,ExtractFiles method, IMsmMerge.ExtractFiles, IMsmMerge::ExtractFiles, _msi_extractfiles_function, mergemod/IMsmMerge::ExtractFiles, setup.imsmmerge_extractfiles
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
 - IMsmMerge::ExtractFiles
 - mergemod/IMsmMerge::ExtractFiles
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
 - IMsmMerge.ExtractFiles
---

# IMsmMerge::ExtractFiles


## -description

The 
<b>ExtractFiles</b> method extracts the embedded .cab file from a module and then writes those files to the destination directory. For more information, see  the 
[ExtractFiles]() method of the 
<a href="/windows/desktop/Msi/merge-object">Merge</a> object.  

<b>IMsmMerge2::ExtractFiles</b>    Mergemod.dll version 2.0 or later.<div> </div><b>IMsmMerge::ExtractFiles</b>      All Mergemod.dll versions.

## -parameters

### -param Path [in]

The fully qualified destination directory. A <b>LPCWSTR</b> may be used in place of a <b>BSTR</b>.

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

<b>ExtractFiles</b> always extracts files using short file names for the path. To use long file names for the path, use the 
<a href="/windows/desktop/api/mergemod/nf-mergemod-imsmmerge2-extractfilesex">ExtractFilesEx</a> function.

## -see-also

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>