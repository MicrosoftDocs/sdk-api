---
UID: NF:vswriter.IVssComponent.GetAlternateLocationMapping
title: IVssComponent::GetAlternateLocationMapping (vswriter.h)
description: The GetAlternateLocationMapping is used to return a file set's alternate location for file restoration. This method can be called by either a writer or a requester.
helpviewer_keywords: ["GetAlternateLocationMapping","GetAlternateLocationMapping method [VSS]","GetAlternateLocationMapping method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetAlternateLocationMapping method","IVssComponent.GetAlternateLocationMapping","IVssComponent::GetAlternateLocationMapping","_win32_ivsscomponent_getalternatelocationmapping","base.ivsscomponent_getalternatelocationmapping","vswriter/IVssComponent::GetAlternateLocationMapping"]
old-location: base\ivsscomponent_getalternatelocationmapping.htm
tech.root: base
ms.assetid: 8c6537eb-67ba-4d6a-ac86-44da176ef5c5
ms.date: 12/05/2018
ms.keywords: GetAlternateLocationMapping, GetAlternateLocationMapping method [VSS], GetAlternateLocationMapping method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetAlternateLocationMapping method, IVssComponent.GetAlternateLocationMapping, IVssComponent::GetAlternateLocationMapping, _win32_ivsscomponent_getalternatelocationmapping, base.ivsscomponent_getalternatelocationmapping, vswriter/IVssComponent::GetAlternateLocationMapping
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
 - IVssComponent::GetAlternateLocationMapping
 - vswriter/IVssComponent::GetAlternateLocationMapping
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
 - IVssComponent.GetAlternateLocationMapping
---

# IVssComponent::GetAlternateLocationMapping


## -description

The 
<b>GetAlternateLocationMapping</b> is used to return a file set's alternate location for file restoration. This method can be called by either a writer or a requester.

## -parameters

### -param iMapping [in]

Index of a particular mapping. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of alternate location mappings associated with the current component. The value of <i>n</i> is returned by 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount">IVssComponent::GetAlternateLocationMappingCount</a>.

### -param ppFiledesc [out]

Doubly indirect pointer to a 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object containing the mapping information.

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
Successfully returned the attribute value.

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
The specified item was not found.

</td>
</tr>
</table>

## -remarks

Alternate location mappings returned by 
<b>GetAlternateLocationMapping</b> can come not only from files in the current component, but also from files in any of its nonselectable subcomponents.

The value returned by <b>IVssComponent::GetAlternateLocationMapping</b> should also not be confused with that returned by 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping">IVssExamineWriterMetadata::GetAlternateLocationMapping</a>:

<ul>
<li>
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping">IVssExamineWriterMetadata::GetAlternateLocationMapping</a> is the alternate location mapping to which a file may be restored if necessary.</li>
<li><b>IVssComponent::GetAlternateLocationMapping</b> is the alternate location to which a file was in fact restored.</li>
</ul>
A file should always be restored to its alternate location mapping if either of the following is true:

<ul>
<li>The restore method (set at backup time) is VSS_RME_RESTORE_TO_ALTERNATE_LOCATION.</li>
<li>Its restore target was set (at restore time) to VSS_RT_ALTERNATE.</li>
</ul>
In either case, having no alternate location mapping defined constitutes a writer error.

A file can be restored to an alternate location mapping if either of the following is true:

<ul>
<li>The restore method is VSS_RME_RESTORE_IF_NOT_THERE and a version of the file is already present on disk.</li>
<li>The restore method is VSS_RME_RESTORE_IF_CAN_REPLACE and a version of the file is present on disk and cannot be replaced.</li>
</ul>
An alternate location mapping is used only during a restore operation and should not be confused with an alternate path, which is used only during a backup operation.

The mapping returned by 
<b>GetAlternateLocationMapping</b> refers to the alternate location mappings used in the course of restoring files.

Alternate location mappings are added to an 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a> object by 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping">IVssBackupComponents::AddAlternativeLocationMapping</a>.

The caller must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release the system resources held by the <i>ppMapping</i> parameter when it is done with the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object that it points to.

For more information on backup and restore file locations under VSS, see 
<a href="/windows/desktop/VSS/non-default-backup-and-restore-locations">Non-Default Backup And Restore Locations</a>.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping">IVssBackupComponents::AddAlternativeLocationMapping</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping">IVssExamineWriterMetadata::GetAlternateLocationMapping</a>