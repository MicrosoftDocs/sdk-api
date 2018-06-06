---
UID: NL:vsbackup.IVssExamineWriterMetadataEx
title: IVssExamineWriterMetadataEx
author: windows-sdk-content
description: Provides a method to retrieve the writer instance name and other basic information for a specific writer instance.
old-location: base\ivssexaminewritermetadataex.htm
old-project: VSS
ms.assetid: 363c987c-7d6c-4efe-988a-1b288f9b4d3c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IVssExamineWriterMetadataEx, IVssExamineWriterMetadataEx interface [VSS], IVssExamineWriterMetadataEx interface [VSS],described, base.ivssexaminewritermetadataex, vsbackup/IVssExamineWriterMetadataEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
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
tech.root: 
req.typenames: AMVPSIZE, *LPAMVPSIZE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsBackup.h
api_name:
 - IVssExamineWriterMetadataEx
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: VssApi.dll
req.irql: 
req.product: Windows UI
---

# IVssExamineWriterMetadataEx class


## -description


The <b>IVssExamineWriterMetadataEx</b> interface is a C++ (not COM) interface that provides a method to retrieve the writer instance name and other basic information for a specific writer instance.

To obtain an instance of the <b>IVssExamineWriterMetadataEx</b> 
   interface, call the <a href="_com_iunknown_queryinterface">QueryInterface</a> method of the 
   <a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a> interface, passing 
   <b>IID_IVssExamineWriterMetadataEx</b> as the interface identifier (IID) parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssExamineWriterMetadataEx</b> interface inherits from <a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a>. <b>IVssExamineWriterMetadataEx</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f36cfa0e-b51e-488b-89b1-99544e2883d9">GetIdentityEx</a>
</td>
<td align="left" width="63%">
Obtains the writer instance name and other basic information about a specific writer instance.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a>
 

 

