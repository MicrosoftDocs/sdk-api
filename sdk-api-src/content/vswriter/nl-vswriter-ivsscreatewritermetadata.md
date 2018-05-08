---
UID: NL:vswriter.IVssCreateWriterMetadata
title: IVssCreateWriterMetadata
author: windows-driver-content
description: The IVssCreateWriterMetadata interface is a C++ (not COM) interface containing methods to construct the Writer Metadata Document in response to an Identify event. It is used only in the CVssWriter::OnIdentify method.
old-location: base\ivsscreatewritermetadata.htm
old-project: VSS
ms.assetid: 427ed302-c3b7-483a-aa48-da6fec1160a9
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IVssCreateWriterMetadata, IVssCreateWriterMetadata interface [VSS], IVssCreateWriterMetadata interface [VSS],described, _win32_ivsscreatewritermetadata, base.ivsscreatewritermetadata, vswriter/IVssCreateWriterMetadata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: class
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
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssCreateWriterMetadata
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssCreateWriterMetadata class


## -description


The 
<b>IVssCreateWriterMetadata</b> interface is a C++ (not COM) interface containing methods to construct the Writer Metadata Document in response to an <a href="vssgloss_i.htm">Identify</a> event. It is used only in 
the <a href="https://msdn.microsoft.com/542d479a-695a-4b1f-94e7-f2ffa08440b7">CVssWriter::OnIdentify</a> method.

The addition and specification of components by a writer is managed through this interface.

After it is constructed, the Writer Metadata Document is a read-only object that requesters query for information about a writer and its components.

<b>IVssCreateWriterMetadata</b> defines the following methods.<table>
<tr>
<th>Method</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/966c40d4-8c19-43cc-ba49-028763478f49">AddAlternateLocationMapping</a>
</td>
<td>Creates an alternate location mapping.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/fdbcbcea-d49e-49bc-9bb8-2210a9de02a4">AddComponent</a>
</td>
<td>Adds a database or file group as a component to be backed up.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/cc6c8ab6-3706-4c75-ba31-cc8c1dc4dd06">AddComponentDependency</a>
</td>
<td>Indicates that a component participates in a backup or restore only if specified components managed by other writers also participate.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/37ef5e50-127d-4bd0-9d26-04dc7781b3ff">AddDatabaseFiles</a>
</td>
<td>Indicates the physical files that are associated with a database to be backed up, as well as their location.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/09bdbdf3-d757-4d3c-8b8b-f792b6cd4ef1">AddDatabaseLogFiles</a>
</td>
<td>Indicates the log files that are associated with a database to be backed up, as well as their location.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/705bb666-9080-4b42-af58-9cc21fbf88cf">AddExcludeFiles</a>
</td>
<td>Specifies the files that will be excluded from the backup.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/5d5a0155-467c-4c42-876e-a1b245cf6f8e">AddFilesToFileGroup</a>
</td>
<td>Adds the specified file or files to the specified file group.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3e84f608-73a7-448b-b45e-a0c348238251">AddIncludeFiles</a>
</td>
<td>Reserved for system use.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/defc7c83-9c40-4661-b8d3-1abdd1be0df4">GetDocument</a>
</td>
<td>Reserved for system use.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/0894912b-85e3-4a5b-bf1b-6bbfe8c9e820">SaveAsXML</a>
</td>
<td>Saves a text string containing the Writer Metadata Document.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/7449fcc8-76fc-4cc5-923c-9a5d53d2cd6b">SetBackupSchema</a>
</td>
<td>Sets the backup schema (how a backup is to be executed) to be used when processing a writer's files.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/0e04df40-49e4-4f23-b4d5-d6b602162935">SetRestoreMethod</a>
</td>
<td>Indicates how writer data is to be restored.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a>
 

 

