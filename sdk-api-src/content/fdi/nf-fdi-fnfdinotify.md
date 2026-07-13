---
UID: NF:fdi.FNFDINOTIFY
title: FNFDINOTIFY macro (fdi.h)
description: The FNFDINOTIFY macro provides the declaration for the application-defined callback notification function to update the application on the status of the decoder.
helpviewer_keywords: ["FNFDINOTIFY","FNFDINOTIFY macro [Windows API]","fdi/FNFDINOTIFY","fdintCABINET_INFO","fdintCLOSE_FILE_INFO","fdintCOPY_FILE","fdintENUMERATE","fdintNEXT_CABINET","fdintPARTIAL_FILE","winprog.fnfdinotify"]
old-location: winprog\fnfdinotify.htm
tech.root: winprog
ms.assetid: 7655ddb2-7cd4-4012-913c-9909fcea639a
ms.date: 12/05/2018
ms.keywords: FNFDINOTIFY, FNFDINOTIFY macro [Windows API], fdi/FNFDINOTIFY, fdintCABINET_INFO, fdintCLOSE_FILE_INFO, fdintCOPY_FILE, fdintENUMERATE, fdintNEXT_CABINET, fdintPARTIAL_FILE, winprog.fnfdinotify
req.header: fdi.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FNFDINOTIFY
 - fdi/FNFDINOTIFY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fdi.h
api_name:
 - FNFDINOTIFY
---

## -description

The <b>FNFDINOTIFY</b> macro provides the declaration for the application-defined callback notification function to update the application on the status of the decoder.

## -parameters

### -param fn

The type of notification.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="fdintCABINET_INFO"></a><a id="fdintcabinet_info"></a><a id="FDINTCABINET_INFO"></a><dl>
<dt><b>fdintCABINET_INFO</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
General information about the cabinet.

When this value is set, the <a href="/windows/desktop/api/fdi/ns-fdi-fdinotification">FDINOTIFICATION</a>  structure is populated with the following information:

<ul>
<li><b>psz1</b> will point to the name of the next cabinet (excluding path information)</li>
<li><b>psz2</b> will point to the name of the next disk</li>
<li><b>psz3</b> will point to the cabinet path name</li>
<li><b>setID</b> will equal the set ID of the current cabinet</li>
<li><b>iCabinet</b> will equal the cabinet number within the cabinet set (0 for the first cabinet, 1 for the second cabinet, etc.)</li>
</ul>
The application should return 0 to indicate success, or -1 to indicate failure, which will abort FDICopy. An <b>fdintCABINET_INFO</b> notification will be provided once for each cabinet opened by <a href="/windows/desktop/api/fdi/nf-fdi-fdicopy">FDICopy</a>; this includes continuation cabinets opened due to files spanning cabinet boundaries.

</td>
</tr>
<tr>
<td width="40%"><a id="fdintPARTIAL_FILE"></a><a id="fdintpartial_file"></a><a id="FDINTPARTIAL_FILE"></a><dl>
<dt><b>fdintPARTIAL_FILE</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
First file in the cabinet is a continuation of a file from previous cabinet.

When this value is set, the <a href="/windows/desktop/api/fdi/ns-fdi-fdinotification">FDINOTIFICATION</a> structure is populated with the following information:

<ul>
<li><b>psz1</b> will point to the name of the file continued from a previous cabinet</li>
<li><b>psz2</b> will point to the name of the cabinet on which the first segment of the file exists</li>
<li><b>psz3</b> will point to the name of the disk on which the first segment of the file exists</li>
</ul>
The <b>fdintPARTIAL_FILE</b> notification is called for files at the beginning of a cabinet that have continued from a previous cabinet. This notification will occur only when <a href="/windows/desktop/api/fdi/nf-fdi-fdicopy">FDICopy</a> is started on the second or subsequent cabinet in a series, which has files continued from a previous cabinet. The application should return 0 for success, or -1  to indicate failure.

</td>
</tr>
<tr>
<td width="40%"><a id="fdintCOPY_FILE"></a><a id="fdintcopy_file"></a><a id="FDINTCOPY_FILE"></a><dl>
<dt><b>fdintCOPY_FILE</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Information identifying the file to be copied.

When this value is set, the <a href="/windows/desktop/api/fdi/ns-fdi-fdinotification">FDINOTIFICATION</a> structure is populated with the following information:

<ul>
<li><b>psz1</b> will point to the name of a file in the cabinet</li>
<li><b>cb</b> will equal the uncompressed size of the file</li>
<li><b>date</b> will equal the file's 16-bit MS-DOS date</li>
<li><b>time</b> will equal the file's 16-bit MS-DOS time</li>
<li><b>attribs</b> will equal the file's 16-bit MS-DOS attributes. Furthermore, the <b>_A_NAME_IS_UTF</b> flag is set if the file name is intended to be interpreted as UTF-8.</li>
</ul>

Note that the above members come directly from the cabinet file.
If the cabinet file is malicious, the name may contain illegal or malicious file name characters.

The application should return one of three values; 0 to skip (i.e. not copy) the file; -1 (negative one) to abort <a href="/windows/desktop/api/fdi/nf-fdi-fdicopy">FDICopy</a>; or a nonzero (and non-negative-one) file handle that indicates where to write the file. The file handle must be compatible with the <a href="/windows/desktop/api/fdi/nf-fdi-fnclose">PFNCLOSE</a> function supplied to <a href="/windows/desktop/api/fdi/nf-fdi-fdicreate">FDICreate</a>. The <b>fdintCOPY_FILE</b> notification is called for each file that starts within the current cabinet, providing the opportunity for the application to request that the file be copied or skipped.

</td>
</tr>
<tr>
<td width="40%"><a id="fdintCLOSE_FILE_INFO"></a><a id="fdintclose_file_info"></a><a id="FDINTCLOSE_FILE_INFO"></a><dl>
<dt><b>fdintCLOSE_FILE_INFO</b></dt>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
Close the file, set relevant information.

When this value is set, the <a href="/windows/desktop/api/fdi/ns-fdi-fdinotification">FDINOTIFICATION</a> structure is populated with the following information:

<ul>
<li><b>psz1</b> will point to the name of a file in the cabinet</li>
<li><b>hf</b> will be a file handle (which originated from <b>fdintCOPY_FILE</b>)</li>
<li><b>date</b> date will equal the file's 16-bit MS-DOS date</li>
<li><b>time</b> time will equal the file's 16-bit MS-DOS time</li>
<li><b>attribs</b> attributes will equal the file's 16-bit MS-DOS attributes (minus the _A_EXEC bit)</li>
<li><b>cb</b> will equal either 0 or 1, indicating whether the file should be executed after extract (1), or not (0)</li>
</ul>
It is the responsibility of the application to execute the file if <b>cb</b> equals 1. The <b>fdintCLOSE_FILE_INFO</b> notification is called after all of the data has been written to a target file. The application must close the file (using the provided <b>hf</b> handle), and set the file date, time, and attributes. The application should return <b>TRUE</b> for success, and <b>FALSE</b> or -1 to abort <a href="/windows/desktop/api/fdi/nf-fdi-fdicopy">FDICopy</a>. FDI assumes that the target file was closed, even if this callback returns failure; FDI will not attempt to use <a href="/windows/desktop/api/fdi/nf-fdi-fnclose">PFNCLOSE</a> to close the file.

</td>
</tr>
<tr>
<td width="40%"><a id="fdintNEXT_CABINET"></a><a id="fdintnext_cabinet"></a><a id="FDINTNEXT_CABINET"></a><dl>
<dt><b>fdintNEXT_CABINET</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
File continued to next cabinet.

When this value is set, the <a href="/windows/desktop/api/fdi/ns-fdi-fdinotification">FDINOTIFICATION</a> structure is populated with the following information: 

<ul>
<li><b>psz1</b> will point to the name of the next cabinet on which the current file is continued</li>
<li><b>psz2</b> will be a file handle (which originated from <b>fdintCOPY_FILE</b>)</li>
<li><b>psz3</b> will point to the cabinet path information</li>
<li><b>fdie</b> will equal a success or error value</li>
</ul>
This notification is called only if <b>fdintCOPY_FILE</b> is instructed to copy a file, which is continued from a subsequent cabinet, to the current cabinet . Since it is possible for the application to modify the cabinet name, it is important that the cabinet path name, indicated by <b>psz3</b>, be validated before it is returned. Additionally, the application should ensure that the cabinet exists and is readable before returning; if necessary, the application should issue a disk change prompt to confirm.

When this function returns to FDI, FDI will verify that the <b>setID</b> and <b>iCabinet</b> fields of the supplied cabinet match the expected values for that cabinet. If not, FDI will continue to send <b>fdintNEXT_CABINET</b> notification messages with the <i>fdie</i> field set to <b>FDIERROR_WRONG_CABINET</b>, until the correct cabinet file is specified, or until this function returns -1 and aborts the <a href="/windows/desktop/api/fdi/nf-fdi-fdicopy">FDICopy</a> call. If, after returning from this function, the cabinet file is not present, readable, or has been damaged, then the <i>fdie</i> field will equal one of the following values:

<ul>
<li><b>FDIERROR_CABINET_NOT_FOUND</b></li>
<li><b>FDIERROR_NOT_A_CABINET</b></li>
<li><b>FDIERROR_UNKNOWN_CABINET_VERSION</b></li>
<li><b>FDIERROR_CORRUPT_CABINET</b></li>
<li><b>FDIERROR_BAD_COMPR_TYPE</b></li>
<li><b>FDIERROR_RESERVE_MISMATCH</b></li>
<li><b>FDIERROR_WRONG_CABINET</b></li>
</ul>
If there was no error, <i>fdie</i> will equal FDIERROR_NONE. The application should return 0 to indicate success, or -1 to indicate failure, which will abort <a href="/windows/desktop/api/fdi/nf-fdi-fdicopy">FDICopy</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="fdintENUMERATE"></a><a id="fdintenumerate"></a><a id="FDINTENUMERATE"></a><dl>
<dt><b>fdintENUMERATE</b></dt>
<dt>0x05</dt>
</dl>
</td>
<td width="60%">
Enumeration status.

</td>
</tr>
</table>
 
## -see-also

<a href="/windows/desktop/api/fdi/nf-fdi-fdicopy">FDICopy</a>



<a href="/windows/desktop/api/fdi/ns-fdi-fdinotification">FDINOTIFICATION</a>