---
UID: NL:vsbackup.IVssExamineWriterMetadataEx2
title: IVssExamineWriterMetadataEx2 (vsbackup.h)
description: Defines methods to retrieve version information and other basic information for a specific writer instance.
helpviewer_keywords: ["IVssExamineWriterMetadataEx2","IVssExamineWriterMetadataEx2 interface","IVssExamineWriterMetadataEx2 interface","described","base.ivssexaminewritermetadataex2","vsbackup/IVssExamineWriterMetadataEx2"]
old-location: base\ivssexaminewritermetadataex2.htm
tech.root: VSS
ms.assetid: 1ef5a83c-8f63-4884-8b70-a8241ba4857b
ms.date: 12/05/2018
ms.keywords: IVssExamineWriterMetadataEx2, IVssExamineWriterMetadataEx2 interface, IVssExamineWriterMetadataEx2 interface,described, base.ivssexaminewritermetadataex2, vsbackup/IVssExamineWriterMetadataEx2
f1_keywords:
- vsbackup/IVssExamineWriterMetadataEx2
dev_langs:
- c++
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- VsBackup.h
api_name:
- IVssExamineWriterMetadataEx2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssExamineWriterMetadataEx2 class


## -description


Defines methods to retrieve version information and other basic information for a specific writer instance.

Your writer application should implement this interface only if you need to use the <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadataex2-getexcludefromsnapshotcount">GetExcludeFromSnapshotCount</a>, <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadataex2-getexcludefromsnapshotfile">GetExcludeFromSnapshotFile</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadataex2-getversion">GetVersion</a> methods. Otherwise, your writer application should implement  the <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadataex">IVssExamineWriterMetadataEx</a> interface or the <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a> interface instead.

The <b>IVssExamineWriterMetadataEx2</b> interface is a C++ (not COM) interface.

To obtain an instance of the <b>IVssExamineWriterMetadataEx2</b> 
   interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of the 
   <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a> interface, and pass  
   the <b>IID_IVssExamineWriterMetadataEx2</b> constant as the interface identifier (IID) parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssExamineWriterMetadataEx2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadataex">IVssExamineWriterMetadataEx</a>. <b>IVssExamineWriterMetadataEx2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssExamineWriterMetadataEx2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadataex2-getexcludefromsnapshotcount">GetExcludeFromSnapshotCount</a>
</td>
<td align="left" width="63%">
Obtains the number of <a href="https://docs.microsoft.com/windows/desktop/VSS/vssgloss-f">file sets</a> that have been explicitly excluded from a given shadow copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadataex2-getexcludefromsnapshotfile">GetExcludeFromSnapshotFile</a>
</td>
<td align="left" width="63%">
Obtains information about <a href="https://docs.microsoft.com/windows/desktop/VSS/vssgloss-f">file sets</a> that have been explicitly excluded from a given shadow copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadataex2-getversion">GetVersion</a>
</td>
<td align="left" width="63%">
Obtains the version information for a writer application.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadataex">IVssExamineWriterMetadataEx</a>
 

 

