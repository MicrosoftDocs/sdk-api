---
UID: NF:vsbackup.IVssExamineWriterMetadataEx2.GetVersion
title: IVssExamineWriterMetadataEx2::GetVersion (vsbackup.h)
description: Obtains the version information for a writer application.
helpviewer_keywords: ["GetVersion","GetVersion method","GetVersion method","IVssExamineWriterMetadataEx2 interface","IVssExamineWriterMetadataEx2 interface","GetVersion method","IVssExamineWriterMetadataEx2.GetVersion","IVssExamineWriterMetadataEx2::GetVersion","base.ivssexaminewritermetadataex2_getversion","vsbackup/IVssExamineWriterMetadataEx2::GetVersion"]
old-location: base\ivssexaminewritermetadataex2_getversion.htm
tech.root: base
ms.assetid: d702263e-0ea5-428c-bbd6-1ab8a7334a92
ms.date: 12/05/2018
ms.keywords: GetVersion, GetVersion method, GetVersion method,IVssExamineWriterMetadataEx2 interface, IVssExamineWriterMetadataEx2 interface,GetVersion method, IVssExamineWriterMetadataEx2.GetVersion, IVssExamineWriterMetadataEx2::GetVersion, base.ivssexaminewritermetadataex2_getversion, vsbackup/IVssExamineWriterMetadataEx2::GetVersion
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssExamineWriterMetadataEx2::GetVersion
 - vsbackup/IVssExamineWriterMetadataEx2::GetVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssExamineWriterMetadataEx2.GetVersion
---

# IVssExamineWriterMetadataEx2::GetVersion


## -description

Obtains the version information for a writer application.

## -parameters

### -param pdwMajorVersion [out]

A pointer to the major version of the writer application.

### -param pdwMinorVersion [out]

A pointer to the minor version of the writer application.

## -returns

The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The writer version information was successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>

## -remarks

The <b>GetVersion</b> method returns nonzero results only if the writer was initialized by calling the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex-initializeex">CVssWriterEx::InitializeEx</a> method and explicit version information was specified. If the writer is initialized by calling the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">CVssWriter::Initialize</a> method, or if no version information was specified in the call to the <b>CVssWriterEx::InitializeEx</b> method, the <b>GetVersion</b> method returns zero in the <i>pdwMajorVersion</i> and <i>pdwMinorVersion</i> parameters.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">CVssWriter::Initialize</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex-initializeex">CVssWriterEx::InitializeEx</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadataex2">IVssExamineWriterMetadataEx2</a>