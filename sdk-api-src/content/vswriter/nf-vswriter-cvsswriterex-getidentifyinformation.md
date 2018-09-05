---
UID: NF:vswriter.CVssWriterEx.GetIdentifyInformation
title: CVssWriterEx::GetIdentifyInformation
author: windows-sdk-content
description: Obtains the metadata that the writer's OnIdentify or OnIdentifyEx method previously reported.
old-location: base\cvsswriterex_getidentifyinformation.htm
old-project: VSS
ms.assetid: 995f353b-d0dc-425a-861d-46b7ee6062da
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CVssWriterEx interface,GetIdentifyInformation method, CVssWriterEx.GetIdentifyInformation, CVssWriterEx::GetIdentifyInformation, GetIdentifyInformation, GetIdentifyInformation method, GetIdentifyInformation method,CVssWriterEx interface, base.cvsswriterex_getidentifyinformation, vswriter/CVssWriterEx::GetIdentifyInformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.redist: 
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
tech.root: 
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - CVssWriterEx.GetIdentifyInformation
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# CVssWriterEx::GetIdentifyInformation


## -description


Obtains the metadata that the writer's <a href="https://msdn.microsoft.com/542d479a-695a-4b1f-94e7-f2ffa08440b7">OnIdentify</a> or <a href="https://msdn.microsoft.com/4cb3b8f6-f702-4fba-a3cc-af84897cfd82">OnIdentifyEx</a> method previously reported.

<b>GetIdentifyInformation</b> is a protected method that is implemented by the 
<a href="https://msdn.microsoft.com/29820c1d-2add-402d-a9ca-9e8674d85f7f">CVssWriterEx</a> base class.


## -parameters




### -param ppMetadata [out]

A doubly indirect pointer to an 
<a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a> object that contains the returned metadata. Writers must not set the returned pointer to <b>NULL</b> or call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> on it, because the VSS service holds a reference to the object.


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
<a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a> object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There was an internal error in the writer.

</td>
</tr>
</table>
 




## -remarks



The <b>GetIdentifyInformation</b> method can only be called in a writer's <a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">OnPrepareBackup</a>, <a href="https://msdn.microsoft.com/a077323e-d04c-4bf7-8aa6-5028fa1c6e6b">OnPrepareSnapshot</a>, or <a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">OnPostSnapshot</a> method.




## -see-also




<a href="https://msdn.microsoft.com/29820c1d-2add-402d-a9ca-9e8674d85f7f">CVssWriterEx</a>
 

 

