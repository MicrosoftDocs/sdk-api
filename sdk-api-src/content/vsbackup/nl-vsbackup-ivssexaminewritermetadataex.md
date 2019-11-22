---
UID: NL:vsbackup.IVssExamineWriterMetadataEx
title: IVssExamineWriterMetadataEx (vsbackup.h)

description: Provides a method to retrieve the writer instance name and other basic information for a specific writer instance.
old-location: base\ivssexaminewritermetadataex.htm
tech.root: VSS
ms.assetid: 363c987c-7d6c-4efe-988a-1b288f9b4d3c

ms.date: 12/05/2018
ms.keywords: IVssExamineWriterMetadataEx, IVssExamineWriterMetadataEx interface [VSS], IVssExamineWriterMetadataEx interface [VSS],described, base.ivssexaminewritermetadataex, vsbackup/IVssExamineWriterMetadataEx
ms.topic: class
f1_keywords: 
 - "vsbackup/IVssExamineWriterMetadataEx"
dev_langs:
 - c++
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
 - IVssExamineWriterMetadataEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssExamineWriterMetadataEx class


## -description


The <b>IVssExamineWriterMetadataEx</b> interface is a C++ (not COM) interface that provides a method to retrieve the writer instance name and other basic information for a specific writer instance.

To obtain an instance of the <b>IVssExamineWriterMetadataEx</b> 
   interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method of the 
   <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a> interface, passing 
   <b>IID_IVssExamineWriterMetadataEx</b> as the interface identifier (IID) parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssExamineWriterMetadataEx</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a>. <b>IVssExamineWriterMetadataEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssExamineWriterMetadataEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadataex-getidentityex">GetIdentityEx</a>
</td>
<td align="left" width="63%">
Obtains the writer instance name and other basic information about a specific writer instance.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a>
 

 

