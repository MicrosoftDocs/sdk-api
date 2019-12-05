---
UID: NL:vswriter.IVssCreateExpressWriterMetadata
title: IVssCreateExpressWriterMetadata (vswriter.h)
description: The IVssCreateExpressWriterMetadata interface is a COM interface containing methods to construct the Writer Metadata Document for an express writer.
old-location: base\ivsscreateexpresswritermetadata.htm
tech.root: VSS
ms.assetid: 49112cff-9e61-4218-a013-5ae5eb58b534
ms.date: 12/05/2018
ms.keywords: IVssCreateExpressWriterMetadata, IVssCreateExpressWriterMetadata interface, IVssCreateExpressWriterMetadata interface,described, base.ivsscreateexpresswritermetadata, vswriter/IVssCreateExpressWriterMetadata
ms.topic: class
f1_keywords:
- vswriter/IVssCreateExpressWriterMetadata
dev_langs:
- c++
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
- IVssCreateExpressWriterMetadata
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssCreateExpressWriterMetadata class


## -description


The <b>IVssCreateExpressWriterMetadata</b> interface is a COM interface containing methods to construct the Writer Metadata Document for an express writer.

After it is constructed, the Writer Metadata Document is a read-only object that requesters query for information about a writer and its components.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssCreateExpressWriterMetadata</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssCreateExpressWriterMetadata</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssCreateExpressWriterMetadata</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscreateexpresswritermetadata-addcomponent">AddComponent</a>
</td>
<td align="left" width="63%">
Adds a 
    file group to an express writer's set of components to be backed up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscreateexpresswritermetadata-addcomponentdependency">AddComponentDependency</a>
</td>
<td align="left" width="63%">
Allows an express writer to indicate that a component it manages has an explicit writer-component dependency; that is, another component (possibly managed by another writer) must be backed up and restored with it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscreateexpresswritermetadata-addexcludefiles">AddExcludeFiles</a>
</td>
<td align="left" width="63%">
Excludes a file set (a specified file or files) that might otherwise be implicitly included when a component of an express writer is backed up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscreateexpresswritermetadata-addfilestofilegroup">AddFilesToFileGroup</a>
</td>
<td align="left" width="63%">
Adds a file set (a specified file or files) to a specified file group component for an express writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscreateexpresswritermetadata-saveasxml">SaveAsXML</a>
</td>
<td align="left" width="63%">
Stores the Writer Metadata Document that contains an express writer's state information into a specified string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscreateexpresswritermetadata-setbackupschema">SetBackupSchema</a>
</td>
<td align="left" width="63%">
Used by an express writer to indicate in its Writer Metadata Document the types of backup operations it can participate in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscreateexpresswritermetadata-setrestoremethod">SetRestoreMethod</a>
</td>
<td align="left" width="63%">
Specifies how an express writer's data is to be restored.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-ivsscreatewritermetadata">IVssCreateWriterMetadata</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-ivssexpresswriter">IVssExpressWriter</a>
 

 

