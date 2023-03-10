---
UID: NF:vsbackup.IVssExamineWriterMetadata.GetComponent
title: IVssExamineWriterMetadata::GetComponent (vsbackup.h)
description: The GetComponent method obtains a Writer Metadata Document for a specified backup component.
helpviewer_keywords: ["GetComponent","GetComponent method [VSS]","GetComponent method [VSS]","IVssExamineWriterMetadata interface","IVssExamineWriterMetadata interface [VSS]","GetComponent method","IVssExamineWriterMetadata.GetComponent","IVssExamineWriterMetadata::GetComponent","_win32_ivssexaminewritermetadata_getcomponent","base.ivssexaminewritermetadata_getcomponent","vsbackup/IVssExamineWriterMetadata::GetComponent"]
old-location: base\ivssexaminewritermetadata_getcomponent.htm
tech.root: base
ms.assetid: fd03ac7c-8398-4972-85f1-2afe13317950
ms.date: 12/05/2018
ms.keywords: GetComponent, GetComponent method [VSS], GetComponent method [VSS],IVssExamineWriterMetadata interface, IVssExamineWriterMetadata interface [VSS],GetComponent method, IVssExamineWriterMetadata.GetComponent, IVssExamineWriterMetadata::GetComponent, _win32_ivssexaminewritermetadata_getcomponent, base.ivssexaminewritermetadata_getcomponent, vsbackup/IVssExamineWriterMetadata::GetComponent
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
 - IVssExamineWriterMetadata::GetComponent
 - vsbackup/IVssExamineWriterMetadata::GetComponent
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
 - IVssExamineWriterMetadata.GetComponent
---

# IVssExamineWriterMetadata::GetComponent


## -description

The 
<b>GetComponent</b> method obtains a Writer Metadata Document for a specified backup component.

## -parameters

### -param iComponent [in]

Index for a component. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of components supported by a given writer. The value of <i>n</i> is returned by 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getfilecounts">IVssExamineWriterMetadata::GetFileCounts</a>.

### -param ppComponent [out]

Doubly indirect pointer to a 
<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswmcomponent">IVssWMComponent</a> object containing the component information.

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
Successfully returned a pointer to an 
<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswmcomponent">IVssWMComponent</a> interface.

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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified component does not exist.

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

The caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release the resources of the returned 
<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswmcomponent">IVssWMComponent</a> object.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getfilecounts">IVssExamineWriterMetadata::GetFileCounts</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswmcomponent">IVssWMComponent</a>