---
UID: NF:vsbackup.IVssExamineWriterMetadata.GetIdentity
title: IVssExamineWriterMetadata::GetIdentity (vsbackup.h)
description: The GetIdentity method obtains basic information about a specific writer instance.
helpviewer_keywords: ["GetIdentity","GetIdentity method [VSS]","GetIdentity method [VSS]","IVssExamineWriterMetadata interface","IVssExamineWriterMetadata interface [VSS]","GetIdentity method","IVssExamineWriterMetadata.GetIdentity","IVssExamineWriterMetadata::GetIdentity","_win32_ivssexaminewritermetadata_getidentity","base.ivssexaminewritermetadata_getidentity","vsbackup/IVssExamineWriterMetadata::GetIdentity"]
old-location: base\ivssexaminewritermetadata_getidentity.htm
tech.root: base
ms.assetid: 55240ef2-f480-4917-98f9-e88a2e23edea
ms.date: 12/05/2018
ms.keywords: GetIdentity, GetIdentity method [VSS], GetIdentity method [VSS],IVssExamineWriterMetadata interface, IVssExamineWriterMetadata interface [VSS],GetIdentity method, IVssExamineWriterMetadata.GetIdentity, IVssExamineWriterMetadata::GetIdentity, _win32_ivssexaminewritermetadata_getidentity, base.ivssexaminewritermetadata_getidentity, vsbackup/IVssExamineWriterMetadata::GetIdentity
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssExamineWriterMetadata::GetIdentity
 - vsbackup/IVssExamineWriterMetadata::GetIdentity
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
 - IVssExamineWriterMetadata.GetIdentity
---

# IVssExamineWriterMetadata::GetIdentity


## -description

The 
<b>GetIdentity</b> method obtains basic information about a specific writer instance.

## -parameters

### -param pidInstance [out]

The address of a caller-allocated variable that receives the instance identifier of the writer.

### -param pidWriter [out]

The address of a caller-allocated variable that receives the class identifier of the writer.

### -param pbstrWriterName [out]

The address of a caller-allocated variable that receives a string that contains the name of the writer.

### -param pUsage [out]

The address of a caller-allocated variable that receives a 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_usage_type">VSS_USAGE_TYPE</a> enumeration value that specifies how the data managed by the writer is used on the host system.

### -param pSource [out]

The address of a caller-allocated variable that receives a 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_source_type">VSS_SOURCE_TYPE</a> enumeration value that specifies the type of data managed by the writer.

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
Successfully returned the identity information.

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
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more information, see 
<a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

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

The caller must free the memory held by the <i>pbstrWriterName</i> parameter by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

An 
<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a> interface might be from stored writer state information (created by a call to 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-createvssexaminewritermetadata">CreateVssExamineWriterMetadata</a>). If this is the case, then the following are true:

<ul>
<li><i>pidInstance</i> may not mean anything in terms of live writers.</li>
<li>If <i>pidWriter</i> does not match the writer class of any live writer, a requester should not use that writer's components.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-createvssexaminewritermetadata">CreateVssExamineWriterMetadata</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_source_type">VSS_SOURCE_TYPE</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_usage_type">VSS_USAGE_TYPE</a>