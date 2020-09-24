---
UID: NF:vsbackup.IVssExamineWriterMetadata.GetAlternateLocationMapping
title: IVssExamineWriterMetadata::GetAlternateLocationMapping (vsbackup.h)
description: The GetAlternateLocationMapping method obtains a specific alternate location mapping of a file set.
helpviewer_keywords: ["GetAlternateLocationMapping","GetAlternateLocationMapping method [VSS]","GetAlternateLocationMapping method [VSS]","IVssExamineWriterMetadata interface","IVssExamineWriterMetadata interface [VSS]","GetAlternateLocationMapping method","IVssExamineWriterMetadata.GetAlternateLocationMapping","IVssExamineWriterMetadata::GetAlternateLocationMapping","_win32_ivssexaminewritermetadata_getalternatelocationmapping","base.ivssexaminewritermetadata_getalternatelocationmapping","vsbackup/IVssExamineWriterMetadata::GetAlternateLocationMapping"]
old-location: base\ivssexaminewritermetadata_getalternatelocationmapping.htm
tech.root: base
ms.assetid: 1264d4bc-dd45-41e7-9f95-c6e9aebd4d22
ms.date: 12/05/2018
ms.keywords: GetAlternateLocationMapping, GetAlternateLocationMapping method [VSS], GetAlternateLocationMapping method [VSS],IVssExamineWriterMetadata interface, IVssExamineWriterMetadata interface [VSS],GetAlternateLocationMapping method, IVssExamineWriterMetadata.GetAlternateLocationMapping, IVssExamineWriterMetadata::GetAlternateLocationMapping, _win32_ivssexaminewritermetadata_getalternatelocationmapping, base.ivssexaminewritermetadata_getalternatelocationmapping, vsbackup/IVssExamineWriterMetadata::GetAlternateLocationMapping
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
 - IVssExamineWriterMetadata::GetAlternateLocationMapping
 - vsbackup/IVssExamineWriterMetadata::GetAlternateLocationMapping
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
 - IVssExamineWriterMetadata.GetAlternateLocationMapping
---

# IVssExamineWriterMetadata::GetAlternateLocationMapping


## -description

The 
<b>GetAlternateLocationMapping</b> method obtains a specific alternate location mapping of a file set.

## -parameters

### -param iMapping [in]

Index of a particular mapping. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of alternate location mappings associated with a given writer. The value of <i>n</i> is returned by 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod">IVssExamineWriterMetadata::GetRestoreMethod</a>.

### -param ppFiledesc [out]

Doubly indirect pointer to an 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object containing the alternate location mapping information.

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
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> interface.

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
The specified alternate location mapping does not exist.

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

The value returned by <b>IVssExamineWriterMetadata::GetAlternateLocationMapping</b> should not be confused with that returned by 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getalternatelocationmapping">IVssComponent::GetAlternateLocationMapping</a>.


<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getalternatelocationmapping">IVssComponent::GetAlternateLocationMapping</a> is the alternate location to which a file was restored.

<b>IVssExamineWriterMetadata::GetAlternateLocationMapping</b> is the alternate location mapping to which a file may be restored if necessary.

A file should always be restored to its alternate location mapping if either of the following is true:

<ul>
<li>The restore method (set at backup time) is VSS_RME_RESTORE_TO_ALTERNATE_LOCATION.</li>
<li>Its restore target was set (at restore time) to VSS_RT_ALTERNATE.</li>
</ul>
In either case, if no valid alternate location mapping is defined, this constitutes a writer error.

A file may be restored to an alternate location mapping if either of the following is true:

<ul>
<li>The restore method is VSS_RME_RESTORE_IF_NOT_THERE and a version of the file is already present on disk.</li>
<li>The restore method is VSS_RME_RESTORE_IF_CAN_REPLACE and a version of the file is present on disk and cannot be replaced.</li>
</ul>
Again, if no valid alternate location mapping is defined, this constitutes a writer error.

An alternate location mapping is used only during a restore operation and should not be confused with an alternate path, which is used only during a backup operation.

The caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release the resources of the returned 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping">IVssBackupComponents::AddAlternativeLocationMapping</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getalternatelocationmapping">IVssComponent::GetAlternateLocationMapping</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod">IVssExamineWriterMetadata::GetRestoreMethod</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a>