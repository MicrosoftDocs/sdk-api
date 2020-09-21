---
UID: NF:vsbackup.IVssExamineWriterMetadataEx.GetIdentityEx
title: IVssExamineWriterMetadataEx::GetIdentityEx (vsbackup.h)
description: The GetIdentityEx method obtains the writer instance name and other basic information about a specific writer instance.
helpviewer_keywords: ["GetIdentityEx","GetIdentityEx method [VSS]","GetIdentityEx method [VSS]","IVssExamineWriterMetadataEx interface","IVssExamineWriterMetadataEx interface [VSS]","GetIdentityEx method","IVssExamineWriterMetadataEx.GetIdentityEx","IVssExamineWriterMetadataEx::GetIdentityEx","base.ivssexaminewritermetadataex_getidentityex","vsbackup/IVssExamineWriterMetadataEx::GetIdentityEx"]
old-location: base\ivssexaminewritermetadataex_getidentityex.htm
tech.root: base
ms.assetid: f36cfa0e-b51e-488b-89b1-99544e2883d9
ms.date: 12/05/2018
ms.keywords: GetIdentityEx, GetIdentityEx method [VSS], GetIdentityEx method [VSS],IVssExamineWriterMetadataEx interface, IVssExamineWriterMetadataEx interface [VSS],GetIdentityEx method, IVssExamineWriterMetadataEx.GetIdentityEx, IVssExamineWriterMetadataEx::GetIdentityEx, base.ivssexaminewritermetadataex_getidentityex, vsbackup/IVssExamineWriterMetadataEx::GetIdentityEx
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
 - IVssExamineWriterMetadataEx::GetIdentityEx
 - vsbackup/IVssExamineWriterMetadataEx::GetIdentityEx
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
 - IVssExamineWriterMetadataEx.GetIdentityEx
---

# IVssExamineWriterMetadataEx::GetIdentityEx


## -description

The <b>GetIdentityEx</b> method obtains the writer instance name and other basic information about a specific writer instance.

## -parameters

### -param pidInstance [out]

Globally unique identifier (GUID) of the writer instance.

### -param pidWriter [out]

GUID of the writer class.

### -param pbstrWriterName [out]

Pointer to a string specifying the name of the writer.

### -param pbstrInstanceName [out]

Pointer to a string specifying the writer instance name.

### -param pUsage [out]

Pointer to a 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_usage_type">VSS_USAGE_TYPE</a> enumeration value indicating how the data managed by the writer is used on the host system.

### -param pSource [out]

Pointer to a 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_source_type">VSS_SOURCE_TYPE</a> enumeration value indicating the type of data managed by the writer.

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
The XML document is  not valid. Check the event log for details. For more information, see 
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

This method is identical to the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getidentity">IVssExamineWriterMetadata::GetIdentity</a> method except for the <i>pbstrInstanceName</i> parameter.

The <i>pbstrInstanceName</i> parameter is the writer instance name that was specified during writer initialization by <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">CVssWriter::Initialize</a>.

The writer instance name is useful for writers that support running multiple writer instances with the same writer class ID on a single computer. The writer instance name can be used to identify the specific instance. Therefore, the writer must make the instance name unique within the writer class. Also, the writer instance name is expected to persist between backup and restore, and it is used by VSS to correctly restore multiple-instance writers.

The caller must free the memory held by the <i>pbstrWriterName</i> and <i>pbstrInstanceName</i> parameters by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

An 
<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadataex">IVssExamineWriterMetadataEx</a> interface might be from stored writer state information (created by a call to 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-createvssexaminewritermetadata">CreateVssExamineWriterMetadata</a>). If this is the case, then the following are true:

<ul>
<li><i>pidInstance</i> may not mean anything in terms of live writers.</li>
<li>If <i>pidWriter</i> does not match the writer class of any live writer, a requester should not use that writer's components.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">CVssWriter::Initialize</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadataex">IVssExamineWriterMetadataEx</a>