---
UID: NF:vsbackup.CreateVssExamineWriterMetadataInternal
title: CreateVssExamineWriterMetadataInternal function (vsbackup.h)
description: The CreateVssExamineWriterMetadata function (vsbackup.h) creates an IVssExamineWriterMetadata object.
helpviewer_keywords: ["CreateVssExamineWriterMetadata","CreateVssExamineWriterMetadata function [VSS]","CreateVssExamineWriterMetadataInternal","_win32_createvssexaminewritermetadata","base.createvssexaminewritermetadata","vsbackup/CreateVssExamineWriterMetadata","vsbackup/CreateVssExamineWriterMetadataInternal"]
old-location: base\createvssexaminewritermetadata.htm
tech.root: base
ms.assetid: cb322541-d8c0-4a2e-9ce5-453d19ac3fd1
ms.date: 08/09/2022
ms.keywords: CreateVssExamineWriterMetadata, CreateVssExamineWriterMetadata function [VSS], CreateVssExamineWriterMetadataInternal, _win32_createvssexaminewritermetadata, base.createvssexaminewritermetadata, vsbackup/CreateVssExamineWriterMetadata, vsbackup/CreateVssExamineWriterMetadataInternal
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
req.dll: VssApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateVssExamineWriterMetadataInternal
 - vsbackup/CreateVssExamineWriterMetadataInternal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VssApi.dll
api_name:
 - CreateVssExamineWriterMetadata
 - CreateVssExamineWriterMetadataInternal
---

# CreateVssExamineWriterMetadataInternal function


## -description

The <b>CreateVssExamineWriterMetadata</b> 
    function creates an 
    <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a> object. <div class="alert"><b>Note</b>  This function is exported as <b>CreateVssExamineWriterMetadataInternal</b>, but you should call <b>CreateVssExamineWriterMetadata</b>, not <b>CreateVssExamineWriterMetadataInternal</b>.</div>
<div> </div>

## -parameters

### -param bstrXML [in]

An XML string containing a Writer Metadata Document with which to initialize the returned 
      <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a> object.

### -param ppMetadata [out]

A variable that receives an 
      <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a> 
      interface pointer to the object.

## -returns

The return values listed here are in addition to the normal COM HRESULTs that may be returned at any time 
       from the function.

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
Successfully returned a pointer to an 
        <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a> interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient backup privileges or is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document passed in the <i>bstrXML</i> parameter is not 
        valid—that is, either it is not a correctly formed XML string or it does not match the 
        schema.

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

To save a copy of a writer’s Writer Metadata Document into an XML string to pass in the <i>bstrXML</i> parameter, use the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml">IVssExamineWriterMetadata::SaveAsXML</a> method.

To retrieve the latest version of a writer’s Writer Metadata Document, use the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata">IVssBackupComponents::GetWriterMetadata</a> method.

To load a writer metadata document into an existing <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a> object, use the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-loadfromxml">IVssExamineWriterMetadata::LoadFromXML</a> method.

Users should not attempt to modify the contents of the Writer Metadata Document.

The calling application is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release the 
    resources held by 
    the <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a> object when the object 
    is no longer needed.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a>
