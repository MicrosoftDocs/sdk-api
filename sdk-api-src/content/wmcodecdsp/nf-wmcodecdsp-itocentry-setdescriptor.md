---
UID: NF:wmcodecdsp.ITocEntry.SetDescriptor
title: ITocEntry::SetDescriptor
author: windows-sdk-content
description: The SetDescriptor method associates a descriptor with the entry.
old-location: mf\itocentry_setdescriptor.htm
tech.root: medfound
ms.assetid: 09a366a6-fcb4-4a0b-8df1-795360d147b9
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ITocEntry interface [Media Foundation],SetDescriptor method, ITocEntry.SetDescriptor, ITocEntry::SetDescriptor, SetDescriptor, SetDescriptor method [Media Foundation], SetDescriptor method [Media Foundation],ITocEntry interface, codecapi.itocentry_setdescriptor, mf.itocentry_setdescriptor, wmcodecdsp/ITocEntry::SetDescriptor
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
 - ITocEntry.SetDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITocEntry::SetDescriptor


## -description


The <b>SetDescriptor</b> method associates a descriptor with the entry.


## -parameters




### -param pDescriptor [in]

Pointer to a <a href="https://msdn.microsoft.com/05e9bf59-5dd8-410f-8e42-25bfb555dd40">TOC_ENTRY_DESCRIPTOR</a> structure that contains the descriptor.


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




<a href="https://msdn.microsoft.com/bb685d4c-c5ec-413f-b279-25216b2bcee8">GetDescriptor</a>



<a href="https://msdn.microsoft.com/82a1a390-50b1-4699-9baa-60cea322ce7c">ITocEntry</a>
 

 

