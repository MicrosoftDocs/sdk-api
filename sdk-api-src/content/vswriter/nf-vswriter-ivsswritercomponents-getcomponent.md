---
UID: NF:vswriter.IVssWriterComponents.GetComponent
title: IVssWriterComponents::GetComponent
author: windows-sdk-content
description: The GetComponent method returns an IVssComponent interface to one of a given writer's components explicitly stored in the Backup Components Document.
old-location: base\ivsswritercomponents_getcomponent.htm
old-project: VSS
ms.assetid: ee816d83-31f3-47ff-b581-cc4dcd878f22
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetComponent, GetComponent method [VSS], GetComponent method [VSS],IVssWriterComponents interface, IVssWriterComponents interface [VSS],GetComponent method, IVssWriterComponents.GetComponent, IVssWriterComponents::GetComponent, _win32_ivsswritercomponents_getcomponent, base.ivsswritercomponents_getcomponent, vswriter/IVssWriterComponents::GetComponent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IVssWriterComponents.GetComponent
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssWriterComponents::GetComponent


## -description


The 
<b>GetComponent</b> method returns an 
<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a> interface to one of a given writer's components explicitly stored in the Backup Components Document.


## -parameters




### -param iComponent [in]

Number of the component. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of components returned by 
<a href="https://msdn.microsoft.com/ec89438f-4811-42f7-bda0-6df6d1b98f18">IVssWriterComponents::GetComponentCount</a>.


### -param ppComponent [out]

Doubly indirect pointer to an instance of the 
<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a> object that contains component information.


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
Successfully returned the component.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified component was not found.

</td>
</tr>
</table>
 




## -remarks



The caller is responsible for calling <a href="https://msdn.microsoft.com/library/Dd757102(v=VS.85).aspx">IUnknown::Release</a> to release system resources held by the returned 
<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a> object.




## -see-also




<a href="https://msdn.microsoft.com/e8ff2491-014c-43c7-bdce-99ed3b408605">IVssWriterComponents</a>
 

 

