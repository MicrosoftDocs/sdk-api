---
UID: NF:mergemod.IMsmMerge.ExtractCAB
title: IMsmMerge::ExtractCAB (mergemod.h)
description: The ExtractCAB method extracts the embedded .cab file from a module and saves it as the specified file.
helpviewer_keywords: ["ExtractCAB","ExtractCAB method","ExtractCAB method","IMsmMerge interface","IMsmMerge interface","ExtractCAB method","IMsmMerge.ExtractCAB","IMsmMerge::ExtractCAB","_msi_extractcab_function","mergemod/IMsmMerge::ExtractCAB","setup.imsmmerge_extractcab"]
old-location: setup\imsmmerge_extractcab.htm
tech.root: setup
ms.assetid: 3f794dac-6eeb-4c1e-8c23-c9d7384f650f
ms.date: 12/05/2018
ms.keywords: ExtractCAB, ExtractCAB method, ExtractCAB method,IMsmMerge interface, IMsmMerge interface,ExtractCAB method, IMsmMerge.ExtractCAB, IMsmMerge::ExtractCAB, _msi_extractcab_function, mergemod/IMsmMerge::ExtractCAB, setup.imsmmerge_extractcab
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
 - IMsmMerge::ExtractCAB
 - mergemod/IMsmMerge::ExtractCAB
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
 - IMsmMerge.ExtractCAB
---

# IMsmMerge::ExtractCAB


## -description

The 
<b>ExtractCAB</b> method extracts the embedded .cab file from a module and saves it as the specified file. The installer creates this file if it does not already exist and overwrites the file if it does exist. For more information, see the 
<a href="/windows/desktop/Msi/merge-extractcab">ExtractCAB</a> method of the 
<a href="/windows/desktop/Msi/merge-object">Merge</a> object.  

<b>IMsmMerge2::ExtractCAB</b>    Mergemod.dll version 2.0 or later.<div> </div><b>IMsmMerge::ExtractCAB</b>      All Mergemod.dll versions.

## -parameters

### -param FileName [in]

The fully qualified destination file. A <b>LPCWSTR</b> may be used in place of a <b>BSTR</b>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is invalid.

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
Unable to access embedded .cab file.

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

## -see-also

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>