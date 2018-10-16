---
UID: NF:wmcodecdsp.IToc.GetDescriptor
title: IToc::GetDescriptor
author: windows-sdk-content
description: The GetDescriptor method retrieves the descriptor, previously set by SetDescriptor, of the table of contents.
old-location: mf\itoc_getdescriptor.htm
tech.root: medfound
ms.assetid: 4568b50f-a777-4c3d-8c71-66737d24b7cd
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: GetDescriptor, GetDescriptor method [Media Foundation], GetDescriptor method [Media Foundation],IToc interface, IToc interface [Media Foundation],GetDescriptor method, IToc.GetDescriptor, IToc::GetDescriptor, codecapi.itoc_getdescriptor, mf.itoc_getdescriptor, wmcodecdsp/IToc::GetDescriptor
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
 - IToc.GetDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IToc::GetDescriptor


## -description


The <b>GetDescriptor</b> method retrieves the descriptor, previously set by <a href="https://msdn.microsoft.com/55208226-fd2d-48e5-887b-34e95309a770">SetDescriptor</a>, of the table of contents.


## -parameters




### -param pDescriptor [out]

Pointer to a <a href="https://msdn.microsoft.com/a79f75c5-be98-4120-85be-71bedbcc0ea2">TOC_DESCRIPTOR</a> structure that receives the descriptor.


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




<a href="https://msdn.microsoft.com/b12d38c7-b80e-4ca8-9ac5-a116100911d0">IToc</a>
 

 

