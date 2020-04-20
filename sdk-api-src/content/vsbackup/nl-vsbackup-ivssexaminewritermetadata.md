---
UID: NL:vsbackup.IVssExamineWriterMetadata
title: IVssExamineWriterMetadata (vsbackup.h)
description: The IVssExamineWriterMetadata interface is a C++ (not COM) interface that allows a requester to examine the metadata of a specific writer instance.helpviewer_keywords: ["IVssExamineWriterMetadata","IVssExamineWriterMetadata interface [VSS]","IVssExamineWriterMetadata interface [VSS]","described","_win32_ivssexaminewritermetadata","base.ivssexaminewritermetadata","vsbackup/IVssExamineWriterMetadata"]
old-location: base\ivssexaminewritermetadata.htm
tech.root: VSS
ms.assetid: b3aa04d9-7299-4e3a-b092-d07f2de6eefe
ms.date: 12/05/2018
ms.keywords: IVssExamineWriterMetadata, IVssExamineWriterMetadata interface [VSS], IVssExamineWriterMetadata interface [VSS],described, _win32_ivssexaminewritermetadata, base.ivssexaminewritermetadata, vsbackup/IVssExamineWriterMetadata
f1_keywords:
- vsbackup/IVssExamineWriterMetadata
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- VssApi.lib
- VssApi.dll
api_name:
- IVssExamineWriterMetadata
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssExamineWriterMetadata class


## -description


The 
<b>IVssExamineWriterMetadata</b> interface is a C++ (not COM) interface that allows a requester to examine the metadata of a specific writer instance. This metadata may come from a currently executing (live) writer, or it may have been stored as an XML document.

An 
<b>IVssExamineWriterMetadata</b> interface to a live writer's metadata is obtained by a call to 
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata">IVssBackupComponents::GetWriterMetadata</a>.

Metadata obtained from a stored XML document can be examined by an instance of 
<b>IVssExamineWriterMetadata</b> obtained by a call to 
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-createvssexaminewritermetadata">CreateVssExamineWriterMetadata</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssExamineWriterMetadata</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssExamineWriterMetadata</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssExamineWriterMetadata</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping">GetAlternateLocationMapping</a>
</td>
<td align="left" width="63%">
Obtains information about the specified alternate location mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema">GetBackupSchema</a>
</td>
<td align="left" width="63%">
Gets the backup schema (how a backup is to be executed) to be used when processing a writer's files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent">GetComponent</a>
</td>
<td align="left" width="63%">
Obtains information about a specified backup component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getdocument">GetDocument</a>
</td>
<td align="left" width="63%">
Reserved for system use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile">GetExcludeFile</a>
</td>
<td align="left" width="63%">
Obtains the specified file element excluded from the backup.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getfilecounts">GetFileCounts</a>
</td>
<td align="left" width="63%">
Obtains file element information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getidentity">GetIdentity</a>
</td>
<td align="left" width="63%">
Obtains basic information about a specific writer instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getincludefile">GetIncludeFile</a>
</td>
<td align="left" width="63%">
Reserved for system use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod">GetRestoreMethod</a>
</td>
<td align="left" width="63%">
Returns information on how the writer data is to be restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-loadfromxml">LoadFromXML</a>
</td>
<td align="left" width="63%">
Converts the specified string of backup data into writer metadata.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml">SaveAsXML</a>
</td>
<td align="left" width="63%">
Converts the specified string of writer metadata into a string that can be saved as part of the backup.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-ivsscreatewritermetadata">IVssCreateWriterMetadata</a>
 

 

