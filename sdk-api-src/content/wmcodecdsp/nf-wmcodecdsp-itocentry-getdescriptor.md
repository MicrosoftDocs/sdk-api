---
UID: NF:wmcodecdsp.ITocEntry.GetDescriptor
title: ITocEntry::GetDescriptor (wmcodecdsp.h)
author: windows-sdk-content
description: The GetDescriptor method retrieves the descriptor, previously set by a call to SetDescriptor, of the entry.
old-location: mf\itocentry_getdescriptor.htm
tech.root: medfound
ms.assetid: bb685d4c-c5ec-413f-b279-25216b2bcee8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDescriptor, GetDescriptor method [Media Foundation], GetDescriptor method [Media Foundation],ITocEntry interface, ITocEntry interface [Media Foundation],GetDescriptor method, ITocEntry.GetDescriptor, ITocEntry::GetDescriptor, codecapi.itocentry_getdescriptor, mf.itocentry_getdescriptor, wmcodecdsp/ITocEntry::GetDescriptor
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
 - ITocEntry.GetDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITocEntry::GetDescriptor


## -description


The <b>GetDescriptor</b> method retrieves the descriptor, previously set by a call to <a href="https://msdn.microsoft.com/09a366a6-fcb4-4a0b-8df1-795360d147b9">SetDescriptor</a>, of the entry.


## -parameters




### -param pDescriptor [out]

Pointer to a <a href="https://msdn.microsoft.com/05e9bf59-5dd8-410f-8e42-25bfb555dd40">TOC_ENTRY_DESCRIPTOR</a> structure that receives the descriptor.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/82a1a390-50b1-4699-9baa-60cea322ce7c">ITocEntry</a>



<a href="https://msdn.microsoft.com/09a366a6-fcb4-4a0b-8df1-795360d147b9">SetDescriptor</a>
 

 

