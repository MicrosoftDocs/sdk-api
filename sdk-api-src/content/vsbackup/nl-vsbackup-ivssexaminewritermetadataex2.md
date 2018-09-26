---
UID: NL:vsbackup.IVssExamineWriterMetadataEx2
title: IVssExamineWriterMetadataEx2
author: windows-sdk-content
description: Defines methods to retrieve version information and other basic information for a specific writer instance.
old-location: base\ivssexaminewritermetadataex2.htm
tech.root: VSS
ms.assetid: 1ef5a83c-8f63-4884-8b70-a8241ba4857b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IVssExamineWriterMetadataEx2, IVssExamineWriterMetadataEx2 interface, IVssExamineWriterMetadataEx2 interface,described, base.ivssexaminewritermetadataex2, vsbackup/IVssExamineWriterMetadataEx2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssExamineWriterMetadataEx2 class


## -description


Defines methods to retrieve version information and other basic information for a specific writer instance.

Your writer application should implement this interface only if you need to use the <a href="https://msdn.microsoft.com/77f21feb-bd7c-4fd0-820b-9dabb1bcbc89">GetExcludeFromSnapshotCount</a>, <a href="https://msdn.microsoft.com/3df57749-9a26-4187-b1fc-aeb68a4d1d06">GetExcludeFromSnapshotFile</a>, and <a href="https://msdn.microsoft.com/d702263e-0ea5-428c-bbd6-1ab8a7334a92">GetVersion</a> methods. Otherwise, your writer application should implement  the <a href="https://msdn.microsoft.com/363c987c-7d6c-4efe-988a-1b288f9b4d3c">IVssExamineWriterMetadataEx</a> interface or the <a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a> interface instead.

The <b>IVssExamineWriterMetadataEx2</b> interface is a C++ (not COM) interface.

To obtain an instance of the <b>IVssExamineWriterMetadataEx2</b> 
   interface, call the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> method of the 
   <a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a> interface, and pass  
   the <b>IID_IVssExamineWriterMetadataEx2</b> constant as the interface identifier (IID) parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssExamineWriterMetadataEx2</b> interface inherits from <a href="https://msdn.microsoft.com/363c987c-7d6c-4efe-988a-1b288f9b4d3c">IVssExamineWriterMetadataEx</a>. <b>IVssExamineWriterMetadataEx2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/77f21feb-bd7c-4fd0-820b-9dabb1bcbc89">GetExcludeFromSnapshotCount</a>
</td>
<td align="left" width="63%">
Obtains the number of <a href="https://msdn.microsoft.com/en-us/library/Aa384656(v=VS.85).aspx">file sets</a> that have been explicitly excluded from a given shadow copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3df57749-9a26-4187-b1fc-aeb68a4d1d06">GetExcludeFromSnapshotFile</a>
</td>
<td align="left" width="63%">
Obtains information about <a href="https://msdn.microsoft.com/en-us/library/Aa384656(v=VS.85).aspx">file sets</a> that have been explicitly excluded from a given shadow copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d702263e-0ea5-428c-bbd6-1ab8a7334a92">GetVersion</a>
</td>
<td align="left" width="63%">
Obtains the version information for a writer application.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/363c987c-7d6c-4efe-988a-1b288f9b4d3c">IVssExamineWriterMetadataEx</a>
 

 

