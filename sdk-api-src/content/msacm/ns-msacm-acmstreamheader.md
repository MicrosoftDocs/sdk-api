---
UID: NS:msacm.tACMSTREAMHEADER
title: ACMSTREAMHEADER (msacm.h)
description: The ACMSTREAMHEADER structure defines the header used to identify an ACM conversion source and destination buffer pair for a conversion stream.
helpviewer_keywords: ["*LPACMSTREAMHEADER","*PACMSTREAMHEADER","ACMSTREAMHEADER","ACMSTREAMHEADER structure [Windows Multimedia]","ACMSTREAMHEADER_STATUSF_DONE","ACMSTREAMHEADER_STATUSF_INQUEUE","ACMSTREAMHEADER_STATUSF_PREPARED","_win32_ACMSTREAMHEADER_str","msacm/ACMSTREAMHEADER","multimedia.acmstreamheader"]
old-location: multimedia\acmstreamheader.htm
tech.root: Multimedia
ms.assetid: 723e96d8-f098-4e08-862a-a9fea8d2fbe3
ms.date: 12/05/2018
ms.keywords: '*LPACMSTREAMHEADER, *PACMSTREAMHEADER, ACMSTREAMHEADER, ACMSTREAMHEADER structure [Windows Multimedia], ACMSTREAMHEADER_STATUSF_DONE, ACMSTREAMHEADER_STATUSF_INQUEUE, ACMSTREAMHEADER_STATUSF_PREPARED, _win32_ACMSTREAMHEADER_str, msacm/ACMSTREAMHEADER, multimedia.acmstreamheader'
req.header: msacm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: ACMSTREAMHEADER, *PACMSTREAMHEADER, *LPACMSTREAMHEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tACMSTREAMHEADER
 - msacm/tACMSTREAMHEADER
 - PACMSTREAMHEADER
 - msacm/PACMSTREAMHEADER
 - ACMSTREAMHEADER
 - msacm/ACMSTREAMHEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msacm.h
api_name:
 - ACMSTREAMHEADER
---

# ACMSTREAMHEADER structure


## -description

The <b>ACMSTREAMHEADER</b> structure defines the header used to identify an ACM conversion source and destination buffer pair for a conversion stream.

## -struct-fields

### -field cbStruct

Size, in bytes, of the <b>ACMSTREAMHEADER</b> structure. This member must be initialized before the application calls any ACM stream functions using this structure. The size specified in this member must be large enough to contain the base <b>ACMSTREAMHEADER</b> structure.

### -field fdwStatus

Flags giving information about the conversion buffers. This member must be initialized to zero before the application calls the <a href="/windows/desktop/api/msacm/nf-msacm-acmstreamprepareheader">acmStreamPrepareHeader</a> function and should not be modified by the application while the stream header remains prepared.

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="ACMSTREAMHEADER_STATUSF_DONE"></a><a id="acmstreamheader_statusf_done"></a><dl>
<dt><b>ACMSTREAMHEADER_STATUSF_DONE</b></dt>
</dl>
</td>
<td width="60%">
Set by the ACM or driver to indicate that it is finished with the conversion and is returning the buffers to the application.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMSTREAMHEADER_STATUSF_INQUEUE"></a><a id="acmstreamheader_statusf_inqueue"></a><dl>
<dt><b>ACMSTREAMHEADER_STATUSF_INQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Set by the ACM or driver to indicate that the buffers are queued for conversion.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMSTREAMHEADER_STATUSF_PREPARED"></a><a id="acmstreamheader_statusf_prepared"></a><dl>
<dt><b>ACMSTREAMHEADER_STATUSF_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
Set by the ACM to indicate that the buffers have been prepared by using the <a href="/windows/desktop/api/msacm/nf-msacm-acmstreamprepareheader">acmStreamPrepareHeader</a> function.

</td>
</tr>
</table>

### -field dwUser

User data. This can be any instance data specified by the application.

### -field pbSrc

Pointer to the source buffer. This pointer must always refer to the same location while the stream header remains prepared. If an application needs to change the source location, it must unprepare the header and reprepare it with the alternate location.

### -field cbSrcLength

Length, in bytes, of the source buffer pointed to by <b>pbSrc</b>. When the header is prepared, this member must specify the maximum size that will be used in the source buffer. Conversions can be performed on source lengths less than or equal to the original prepared size. However, this member must be reset to the original size when an application unprepares the header.

### -field cbSrcLengthUsed

Amount of data, in bytes, used for the conversion. This member is not valid until the conversion is complete. This value can be less than or equal to <b>cbSrcLength</b>. An application must use the <b>cbSrcLengthUsed</b> member when advancing to the next piece of source data for the conversion stream.

### -field dwSrcUser

User data. This can be any instance data specified by the application.

### -field pbDst

Pointer to the destination buffer. This pointer must always refer to the same location while the stream header remains prepared. If an application needs to change the destination location, it must unprepare the header and reprepare it with the alternate location.

### -field cbDstLength

Length, in bytes, of the destination buffer pointed to by <b>pbDst</b>. When the header is prepared, this member must specify the maximum size that will be used in the destination buffer.

### -field cbDstLengthUsed

Amount of data, in bytes, returned by a conversion. This member is not valid until the conversion is complete. This value can be less than or equal to <b>cbDstLength</b>. An application must use the <b>cbDstLengthUsed</b> member when advancing to the next destination location for the conversion stream.

### -field dwDstUser

User data. This can be any instance data specified by the application.

### -field dwReservedDriver

Reserved; do not use. This member requires no initialization by the application and should never be modified while the header remains prepared.

## -remarks

Before an <b>ACMSTREAMHEADER</b> structure can be used for a conversion, it must be prepared by using the <a href="/windows/desktop/api/msacm/nf-msacm-acmstreamprepareheader">acmStreamPrepareHeader</a> function. When an application is finished with an <b>ACMSTREAMHEADER</b> structure, it must call the <a href="/windows/desktop/api/msacm/nf-msacm-acmstreamunprepareheader">acmStreamUnprepareHeader</a> function before freeing the source and destination buffers.

## -see-also

Audio Compression Manager



<a href="/windows/desktop/Multimedia/audio-compression-structures">Audio Compression Structures</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmstreamprepareheader">acmStreamPrepareHeader</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmstreamunprepareheader">acmStreamUnprepareHeader</a>