---
UID: NF:wmcodecdsp.ITocEntry.GetSubEntries
title: ITocEntry::GetSubEntries
author: windows-sdk-content
description: The GetSubEntries method gets an array of subentry indices that were set by a previous call to SetSubEntries.
old-location: mf\itocentry_getsubentries.htm
tech.root: medfound
ms.assetid: 583340d7-87f9-40c5-a0dc-3e69bbb96334
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: GetSubEntries, GetSubEntries method [Media Foundation], GetSubEntries method [Media Foundation],ITocEntry interface, ITocEntry interface [Media Foundation],GetSubEntries method, ITocEntry.GetSubEntries, ITocEntry::GetSubEntries, codecapi.itocentry_getsubentries, mf.itocentry_getsubentries, wmcodecdsp/ITocEntry::GetSubEntries
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmcodecdsp.h
req.include-header: 
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
req.dll: Wmvdspa.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmvdspa.dll
api_name:
 - ITocEntry.GetSubEntries
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITocEntry::GetSubEntries


## -description


The <b>GetSubEntries</b> method gets an array of subentry indices that were set by a previous call to <a href="https://msdn.microsoft.com/4b3f4038-483c-4f00-a819-ace83d99da58">SetSubEntries</a>.


## -parameters




### -param pdwNumSubEntries [in, out]

If <i>pwSubEntryIndices</i> is <b>NULL</b>, this is an output parameter that receives the number of subentries associated with this entry. If <i>pwSubEntryIndices</i> is not <b>NULL</b>, this is an input parameter that specifies the number of <b>DWORD</b>s in the caller-allocated array pointed to by <i>pwSubEntryIndices</i>.


### -param pwSubEntryIndices [out]

<b>NULL</b>, or a pointer to a caller-allocated array of <b>DWORD</b>s that receives the subentry indices.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The method returns this error code if <i>pwSubEntryIndices</i> is not <b>NULL</b> and the number of subentries is larger than the number specified by <i>pdwNumSubEntries</i>. In that case, <i>pdwNumSubEntries</i> serves as an output parameter and receives the number of available subentry indices.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/82a1a390-50b1-4699-9baa-60cea322ce7c">ITocEntry</a>



<a href="https://msdn.microsoft.com/4b3f4038-483c-4f00-a819-ace83d99da58">SetSubEntries</a>
 

 

