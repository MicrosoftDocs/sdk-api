---
UID: NF:msctf.ITfContextOwnerCompositionServices.TerminateComposition
title: ITfContextOwnerCompositionServices::TerminateComposition
author: windows-sdk-content
description: ITfContextOwnerCompositionServices::TerminateComposition method
old-location: tsf\itfcontextownercompositionservices_terminatecomposition.htm
old-project: TSF
ms.assetid: 950ba2b3-cb12-4697-a4b2-1c87373b9a23
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfContextOwnerCompositionServices interface [Text Services Framework],TerminateComposition method, ITfContextOwnerCompositionServices.TerminateComposition, ITfContextOwnerCompositionServices::TerminateComposition, TerminateComposition, TerminateComposition method [Text Services Framework], TerminateComposition method [Text Services Framework],ITfContextOwnerCompositionServices interface, _tsf_itfcontextownercompositionservices_terminatecomposition_ref, msctf/ITfContextOwnerCompositionServices::TerminateComposition, tsf.itfcontextownercompositionservices_terminatecomposition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfContextOwnerCompositionServices.TerminateComposition
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfContextOwnerCompositionServices::TerminateComposition


## -description




## -parameters




### -param pComposition [in]

Pointer to a <a href="https://msdn.microsoft.com/1c8aac3e-384e-402e-aae8-11e240083603">ITfCompositionView</a> interface that represents the composition to terminate. If this value is <b>NULL</b>, all compositions in the context are terminated.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context is not on a document stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
A text service currently holds a lock on the document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
This method was called during another composition operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



A text service uses <a href="https://msdn.microsoft.com/b5717c03-2611-4199-b07d-b6f3b6f65d3a">ITfComposition::EndComposition</a> to terminate a composition that it created.

If the context owner implements the text store, the context owner must be able to grant a synchronous write lock before calling this method.

This method also does the following:

<ul>
<li>For each composition terminated, <a href="https://msdn.microsoft.com/4b7c3993-6d01-492f-9bb5-241a1cbd4b63">ITfCompositionSink::OnCompositionTerminated</a> is called for all installed composition advise sinks.</li>
<li>If the context owner installed a context owner composition advise sink, <a href="https://msdn.microsoft.com/816aaa81-1b51-4e01-b49c-a9cbe2b87735">ITfContextOwnerCompositionSink::OnEndComposition</a> is called for each terminated composition.</li>
<li>The GUID_PROP_COMPOSING property will be cleared for the text covered by each terminated composition.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b5717c03-2611-4199-b07d-b6f3b6f65d3a">
        ITfComposition::EndComposition
      </a>



<a href="https://msdn.microsoft.com/4b7c3993-6d01-492f-9bb5-241a1cbd4b63">
        ITfCompositionSink::OnCompositionTerminated
      </a>



<a href="https://msdn.microsoft.com/1c8aac3e-384e-402e-aae8-11e240083603">ITfCompositionView
      </a>



<a href="https://msdn.microsoft.com/7c84cffe-dec8-4e24-b00a-e536984f2a10">ITfContextOwnerCompositionServices</a>



<a href="https://msdn.microsoft.com/816aaa81-1b51-4e01-b49c-a9cbe2b87735">
        ITfContextOwnerCompositionSink::OnEndComposition
      </a>
 

 

