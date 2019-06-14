---
UID: NF:vswriter.CVssWriterEx.GetIdentifyInformation
title: CVssWriterEx::GetIdentifyInformation (vswriter.h)
author: windows-sdk-content
description: Obtains the metadata that the writer's OnIdentify or OnIdentifyEx method previously reported.
old-location: base\cvsswriterex_getidentifyinformation.htm
tech.root: VSS
ms.assetid: 995f353b-d0dc-425a-861d-46b7ee6062da
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CVssWriterEx interface,GetIdentifyInformation method, CVssWriterEx.GetIdentifyInformation, CVssWriterEx::GetIdentifyInformation, GetIdentifyInformation, GetIdentifyInformation method, GetIdentifyInformation method,CVssWriterEx interface, base.cvsswriterex_getidentifyinformation, vswriter/CVssWriterEx::GetIdentifyInformation
ms.topic: method
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
 - CVssWriterEx.GetIdentifyInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CVssWriterEx::GetIdentifyInformation


## -description


Obtains the metadata that the writer's <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onidentify">OnIdentify</a> or <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex-onidentifyex">OnIdentifyEx</a> method previously reported.

<b>GetIdentifyInformation</b> is a protected method that is implemented by the 
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-cvsswriterex">CVssWriterEx</a> base class.


## -parameters




### -param ppMetadata [out]

A doubly indirect pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a> object that contains the returned metadata. Writers must not set the returned pointer to <b>NULL</b> or call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on it, because the VSS service holds a reference to the object.


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
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a> object.

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



The <b>GetIdentifyInformation</b> method can only be called in a writer's <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">OnPrepareBackup</a>, <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparesnapshot">OnPrepareSnapshot</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">OnPostSnapshot</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-cvsswriterex">CVssWriterEx</a>
 

 

