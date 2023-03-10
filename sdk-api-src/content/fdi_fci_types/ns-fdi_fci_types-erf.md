---
UID: NS:fdi_fci_types.ERF
title: ERF (fdi_fci_types.h)
description: The ERF structure contains error information from FCI/FDI. The caller should not modify this structure.
helpviewer_keywords: ["*PERF","ERF","ERF FAR *PERF","ERF FAR *PERF structure [Windows API]","ERF structure [Windows API]","FCIERR_ALLOC_FAIL","FCIERR_BAD_COMPR_TYPE","FCIERR_CAB_FILE","FCIERR_CAB_FORMAT_LIMIT","FCIERR_MCI_FAIL","FCIERR_NONE","FCIERR_OPEN_SRC","FCIERR_READ_SRC","FCIERR_TEMP_FILE","FCIERR_USER_ABORT","FDIERROR_ALLOC_FAIL","FDIERROR_BAD_COMPR_TYPE","FDIERROR_CABINET_NOT_FOUND","FDIERROR_CORRUPT_CABINET","FDIERROR_MDI_FAIL","FDIERROR_NONE","FDIERROR_NOT_A_CABINET","FDIERROR_RESERVE_MISMATCH","FDIERROR_TARGET_FILE","FDIERROR_UNKNOWN_CABINET_VERSION","FDIERROR_USER_ABORT","FDIERROR_WRONG_CABINET","fdi_fci_types/ERF","winprog.erf"]
old-location: winprog\erf.htm
tech.root: winprog
ms.assetid: ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b
ms.date: 12/05/2018
ms.keywords: '*PERF, ERF, ERF FAR *PERF, ERF FAR *PERF structure [Windows API], ERF structure [Windows API], FCIERR_ALLOC_FAIL, FCIERR_BAD_COMPR_TYPE, FCIERR_CAB_FILE, FCIERR_CAB_FORMAT_LIMIT, FCIERR_MCI_FAIL, FCIERR_NONE, FCIERR_OPEN_SRC, FCIERR_READ_SRC, FCIERR_TEMP_FILE, FCIERR_USER_ABORT, FDIERROR_ALLOC_FAIL, FDIERROR_BAD_COMPR_TYPE, FDIERROR_CABINET_NOT_FOUND, FDIERROR_CORRUPT_CABINET, FDIERROR_MDI_FAIL, FDIERROR_NONE, FDIERROR_NOT_A_CABINET, FDIERROR_RESERVE_MISMATCH, FDIERROR_TARGET_FILE, FDIERROR_UNKNOWN_CABINET_VERSION, FDIERROR_USER_ABORT, FDIERROR_WRONG_CABINET, fdi_fci_types/ERF, winprog.erf'
req.header: fdi_fci_types.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ERF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ERF
 - fdi_fci_types/ERF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fdi_fci_types.h
api_name:
 - ERF FAR *PERF
---

# ERF structure


## -description

<p class="CCE_Message">[This structure contains information required by the <b>Extract</b> function, which is not supported. This documentation is provided for informational purposes only.]

The <b>ERF</b> structure contains error information from FCI/FDI. The caller should not modify this structure.

## -struct-fields

### -field erfOper

An FCI/FDI error code.


The following values are returned for FCI:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FCIERR_NONE"></a><a id="fcierr_none"></a><dl>
<dt><b>FCIERR_NONE</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
No Error.

</td>
</tr>
<tr>
<td width="40%"><a id="FCIERR_OPEN_SRC"></a><a id="fcierr_open_src"></a><dl>
<dt><b>FCIERR_OPEN_SRC</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Failure opening the file to be stored in the cabinet.

</td>
</tr>
<tr>
<td width="40%"><a id="FCIERR_READ_SRC"></a><a id="fcierr_read_src"></a><dl>
<dt><b>FCIERR_READ_SRC</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Failure reading the file to be stored in the cabinet.

</td>
</tr>
<tr>
<td width="40%"><a id="FCIERR_ALLOC_FAIL"></a><a id="fcierr_alloc_fail"></a><dl>
<dt><b>FCIERR_ALLOC_FAIL</b></dt>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
Out of memory in FCI.

</td>
</tr>
<tr>
<td width="40%"><a id="FCIERR_TEMP_FILE"></a><a id="fcierr_temp_file"></a><dl>
<dt><b>FCIERR_TEMP_FILE</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Could not create a temporary file.

</td>
</tr>
<tr>
<td width="40%"><a id="FCIERR_BAD_COMPR_TYPE"></a><a id="fcierr_bad_compr_type"></a><dl>
<dt><b>FCIERR_BAD_COMPR_TYPE</b></dt>
<dt>0x05</dt>
</dl>
</td>
<td width="60%">
Unknown compression type.

</td>
</tr>
<tr>
<td width="40%"><a id="FCIERR_CAB_FILE"></a><a id="fcierr_cab_file"></a><dl>
<dt><b>FCIERR_CAB_FILE</b></dt>
<dt>0x06</dt>
</dl>
</td>
<td width="60%">
Could not create the cabinet file.

</td>
</tr>
<tr>
<td width="40%"><a id="FCIERR_USER_ABORT"></a><a id="fcierr_user_abort"></a><dl>
<dt><b>FCIERR_USER_ABORT</b></dt>
<dt>0x07</dt>
</dl>
</td>
<td width="60%">
FCI aborted.

</td>
</tr>
<tr>
<td width="40%"><a id="FCIERR_MCI_FAIL"></a><a id="fcierr_mci_fail"></a><dl>
<dt><b>FCIERR_MCI_FAIL</b></dt>
<dt>0x08</dt>
</dl>
</td>
<td width="60%">
Failure compressing data.

</td>
</tr>
<tr>
<td width="40%"><a id="FCIERR_CAB_FORMAT_LIMIT"></a><a id="fcierr_cab_format_limit"></a><dl>
<dt><b>FCIERR_CAB_FORMAT_LIMIT</b></dt>
<dt>0x09</dt>
</dl>
</td>
<td width="60%">
Data-size or file-count exceeded CAB format limits.

</td>
</tr>
</table>
 


The following values are returned for FDI:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FDIERROR_NONE"></a><a id="fdierror_none"></a><dl>
<dt><b>FDIERROR_NONE</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
No error.

</td>
</tr>
<tr>
<td width="40%"><a id="FDIERROR_CABINET_NOT_FOUND"></a><a id="fdierror_cabinet_not_found"></a><dl>
<dt><b>FDIERROR_CABINET_NOT_FOUND</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The cabinet file was  not found.

</td>
</tr>
<tr>
<td width="40%"><a id="FDIERROR_NOT_A_CABINET"></a><a id="fdierror_not_a_cabinet"></a><dl>
<dt><b>FDIERROR_NOT_A_CABINET</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
The cabinet file does not have the correct format.

</td>
</tr>
<tr>
<td width="40%"><a id="FDIERROR_UNKNOWN_CABINET_VERSION"></a><a id="fdierror_unknown_cabinet_version"></a><dl>
<dt><b>FDIERROR_UNKNOWN_CABINET_VERSION</b></dt>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
The cabinet file has an unknown version number.

</td>
</tr>
<tr>
<td width="40%"><a id="FDIERROR_CORRUPT_CABINET"></a><a id="fdierror_corrupt_cabinet"></a><dl>
<dt><b>FDIERROR_CORRUPT_CABINET</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
The cabinet file is corrupt.

</td>
</tr>
<tr>
<td width="40%"><a id="FDIERROR_ALLOC_FAIL"></a><a id="fdierror_alloc_fail"></a><dl>
<dt><b>FDIERROR_ALLOC_FAIL</b></dt>
<dt>0x05</dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%"><a id="FDIERROR_BAD_COMPR_TYPE"></a><a id="fdierror_bad_compr_type"></a><dl>
<dt><b>FDIERROR_BAD_COMPR_TYPE</b></dt>
<dt>0x06</dt>
</dl>
</td>
<td width="60%">
Unknown compression type used in the cabinet folder.

</td>
</tr>
<tr>
<td width="40%"><a id="FDIERROR_MDI_FAIL"></a><a id="fdierror_mdi_fail"></a><dl>
<dt><b>FDIERROR_MDI_FAIL</b></dt>
<dt>0x07</dt>
</dl>
</td>
<td width="60%">
Failure decompressing data from the cabinet file.

</td>
</tr>
<tr>
<td width="40%"><a id="FDIERROR_TARGET_FILE"></a><a id="fdierror_target_file"></a><dl>
<dt><b>FDIERROR_TARGET_FILE</b></dt>
<dt>0x08</dt>
</dl>
</td>
<td width="60%">
Failure writing to the target file.

</td>
</tr>
<tr>
<td width="40%"><a id="FDIERROR_RESERVE_MISMATCH"></a><a id="fdierror_reserve_mismatch"></a><dl>
<dt><b>FDIERROR_RESERVE_MISMATCH</b></dt>
<dt>0x09</dt>
</dl>
</td>
<td width="60%">
The cabinets within a set do not have the same RESERVE sizes.

</td>
</tr>
<tr>
<td width="40%"><a id="FDIERROR_WRONG_CABINET"></a><a id="fdierror_wrong_cabinet"></a><dl>
<dt><b>FDIERROR_WRONG_CABINET</b></dt>
<dt>0x0A</dt>
</dl>
</td>
<td width="60%">
The cabinet returned by fdintNEXT_CABINET is incorrect.

</td>
</tr>
<tr>
<td width="40%"><a id="FDIERROR_USER_ABORT"></a><a id="fdierror_user_abort"></a><dl>
<dt><b>FDIERROR_USER_ABORT</b></dt>
<dt>0x0B</dt>
</dl>
</td>
<td width="60%">
FDI aborted.

</td>
</tr>
</table>

### -field erfType

An optional error value filled in by FCI/FDI. For FCI, this is usually the C runtime errno value.

### -field fError

A flag that indicates an error. If <b>TRUE</b>, an error is present.

## -see-also

<a href="/windows/desktop/DevNotes/extract">Extract</a>

