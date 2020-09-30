---
UID: NL:vswriter.IVssCreateWriterMetadata
title: IVssCreateWriterMetadata (vswriter.h)
description: The IVssCreateWriterMetadata interface is a C++ (not COM) interface containing methods to construct the Writer Metadata Document in response to an Identify event. It is used only in the CVssWriter::OnIdentify method.
helpviewer_keywords: ["IVssCreateWriterMetadata","IVssCreateWriterMetadata interface [VSS]","IVssCreateWriterMetadata interface [VSS]","described","_win32_ivsscreatewritermetadata","base.ivsscreatewritermetadata","vswriter/IVssCreateWriterMetadata"]
old-location: base\ivsscreatewritermetadata.htm
tech.root: base
ms.assetid: 427ed302-c3b7-483a-aa48-da6fec1160a9
ms.date: 12/05/2018
ms.keywords: IVssCreateWriterMetadata, IVssCreateWriterMetadata interface [VSS], IVssCreateWriterMetadata interface [VSS],described, _win32_ivsscreatewritermetadata, base.ivsscreatewritermetadata, vswriter/IVssCreateWriterMetadata
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
 - IVssCreateWriterMetadata
 - vswriter/IVssCreateWriterMetadata
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
 - IVssCreateWriterMetadata
---

# IVssCreateWriterMetadata class


## -description

The 
<b>IVssCreateWriterMetadata</b> interface is a C++ (not COM) interface containing methods to construct the Writer Metadata Document in response to an <a href="/windows/desktop/VSS/vssgloss-i">Identify</a> event. It is used only in 
the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onidentify">CVssWriter::OnIdentify</a> method.

The addition and specification of components by a writer is managed through this interface.

After it is constructed, the Writer Metadata Document is a read-only object that requesters query for information about a writer and its components.

<b>IVssCreateWriterMetadata</b> defines the following methods.<table>
<tr>
<th>Method</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping">AddAlternateLocationMapping</a>
</td>
<td>Creates an alternate location mapping.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addcomponent">AddComponent</a>
</td>
<td>Adds a database or file group as a component to be backed up.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency">AddComponentDependency</a>
</td>
<td>Indicates that a component participates in a backup or restore only if specified components managed by other writers also participate.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles">AddDatabaseFiles</a>
</td>
<td>Indicates the physical files that are associated with a database to be backed up, as well as their location.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles">AddDatabaseLogFiles</a>
</td>
<td>Indicates the log files that are associated with a database to be backed up, as well as their location.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles">AddExcludeFiles</a>
</td>
<td>Specifies the files that will be excluded from the backup.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup">AddFilesToFileGroup</a>
</td>
<td>Adds the specified file or files to the specified file group.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles">AddIncludeFiles</a>
</td>
<td>Reserved for system use.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-getdocument">GetDocument</a>
</td>
<td>Reserved for system use.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-saveasxml">SaveAsXML</a>
</td>
<td>Saves a text string containing the Writer Metadata Document.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema">SetBackupSchema</a>
</td>
<td>Sets the backup schema (how a backup is to be executed) to be used when processing a writer's files.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod">SetRestoreMethod</a>
</td>
<td>Indicates how writer data is to be restored.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a>