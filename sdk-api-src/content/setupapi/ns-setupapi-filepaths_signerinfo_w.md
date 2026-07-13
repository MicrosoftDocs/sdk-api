---
UID: NS:setupapi._FILEPATHS_SIGNERINFO_W
title: FILEPATHS_SIGNERINFO_W (setupapi.h)
description: The FILEPATHS_SINGNERINFO structure stores source and target path information, and also file signature information. (Unicode)
helpviewer_keywords: ["*PFILEPATHS_SIGNERINFO_W","FILEOP_COPY","FILEOP_DELETE","FILEPATHS_SIGNERINFO","FILEPATHS_SIGNERINFO structure [Setup API]","FILEPATHS_SIGNERINFO_W","PFILEPATHS_SIGNERINFO","PFILEPATHS_SIGNERINFO structure pointer [Setup API]","SP_COPY_NOBROWSE","SP_COPY_NOSKIP","SP_COPY_WARNIFSKIP","_setupapi_filepaths_signerinfo","setup.filepaths_signerinfo","setupapi/FILEPATHS_SIGNERINFO","setupapi/PFILEPATHS_SIGNERINFO"]
old-location: setup\filepaths_signerinfo.htm
tech.root: setup
ms.assetid: c651933f-cf61-4012-9d08-195336f2cb3d
ms.date: 12/05/2018
ms.keywords: '*PFILEPATHS_SIGNERINFO_W, FILEOP_COPY, FILEOP_DELETE, FILEPATHS_SIGNERINFO, FILEPATHS_SIGNERINFO structure [Setup API], FILEPATHS_SIGNERINFO_W, PFILEPATHS_SIGNERINFO, PFILEPATHS_SIGNERINFO structure pointer [Setup API], SP_COPY_NOBROWSE, SP_COPY_NOSKIP, SP_COPY_WARNIFSKIP, _setupapi_filepaths_signerinfo, setup.filepaths_signerinfo, setupapi/FILEPATHS_SIGNERINFO, setupapi/PFILEPATHS_SIGNERINFO'
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: FILEPATHS_SIGNERINFO_W, *PFILEPATHS_SIGNERINFO_W
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FILEPATHS_SIGNERINFO_W
 - setupapi/_FILEPATHS_SIGNERINFO_W
 - PFILEPATHS_SIGNERINFO_W
 - setupapi/PFILEPATHS_SIGNERINFO_W
 - FILEPATHS_SIGNERINFO_W
 - setupapi/FILEPATHS_SIGNERINFO_W
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Setupapi.h
api_name:
 - FILEPATHS_SIGNERINFO - filepaths_signerinfo_w
---

# FILEPATHS_SIGNERINFO_W structure


## -description

The <b>FILEPATHS_SINGNERINFO</b> structure stores source and target path information, and also file signature information. The setup functions send 
<b>FILEPATHS_SIGNERINFO</b> as a parameter in several of the notifications sent to callback routines. For more information, see 
<a href="/windows/desktop/SetupApi/notifications">Notifications</a>.

## -struct-fields

### -field Target

Path to the target file.

### -field Source

Path to the source file. This member is not used when the 
<a href="/windows/desktop/api/setupapi/ns-setupapi-filepaths_a">FILEPATHS</a> structure is used with a file delete operation.

### -field Win32Error

If an error occurs, this member is the <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. If no error has occurred, it is  NO_ERROR.

### -field Flags

Additional information that depends on the notification sent with the 
<b>FILEPATHS_SIGNERINFO</b> structure. 




For 
<a href="/windows/desktop/SetupApi/spfilenotify-copyerror">SPFILENOTIFY_COPYERROR</a> notifications, <b>Flags</b> specifies dialog box behavior and can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_NOBROWSE"></a><a id="sp_copy_nobrowse"></a><dl>
<dt><b>SP_COPY_NOBROWSE</b></dt>
</dl>
</td>
<td width="60%">
Do not offer the user the option to browse.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_NOSKIP"></a><a id="sp_copy_noskip"></a><dl>
<dt><b>SP_COPY_NOSKIP</b></dt>
</dl>
</td>
<td width="60%">
Do not offer the user the option to skip the file.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_WARNIFSKIP"></a><a id="sp_copy_warnifskip"></a><dl>
<dt><b>SP_COPY_WARNIFSKIP</b></dt>
</dl>
</td>
<td width="60%">
Inform the user that skipping the file may affect the installation.

</td>
</tr>
</table>
 

For 
<a href="/windows/desktop/SetupApi/spfilenotify-fileopdelayed">SPFILENOTIFY_FILEOPDELAYED</a> notifications, <b>Flags</b> specifies the type of file operation delayed and can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILEOP_COPY"></a><a id="fileop_copy"></a><dl>
<dt><b>FILEOP_COPY</b></dt>
</dl>
</td>
<td width="60%">
A file copy operation was delayed.

</td>
</tr>
<tr>
<td width="40%"><a id="FILEOP_DELETE"></a><a id="fileop_delete"></a><dl>
<dt><b>FILEOP_DELETE</b></dt>
</dl>
</td>
<td width="60%">
A file delete operation was delayed.

</td>
</tr>
</table>

### -field DigitalSigner

Digital signer of the file.

### -field Version

Version of the file.

### -field CatalogFile

Catalog file.

## -see-also

<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/SetupApi/structures--setup-api-">Structures</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines FILEPATHS_SIGNERINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
