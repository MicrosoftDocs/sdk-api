---
UID: NF:mfapi.MFAllocateWorkQueue
title: MFAllocateWorkQueue function
author: windows-sdk-content
description: Creates a new work queue.
old-location: mf\mfallocateworkqueue.htm
tech.root: medfound
ms.assetid: 8def4375-919c-4619-9484-9ce2708a3886
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 8def4375-919c-4619-9484-9ce2708a3886, MFAllocateWorkQueue, MFAllocateWorkQueue function [Media Foundation], mf.mfallocateworkqueue, mfapi/MFAllocateWorkQueue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFAllocateWorkQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFAllocateWorkQueue function


## -description


Creates a new work queue.


## -parameters




### -param pdwWorkQueue [out]

Receives an identifier for the work queue.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The application exceeded the maximum number of work queues.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The application did not call <a href="https://msdn.microsoft.com/b4472e40-3681-4b26-9385-4df7bf19c2d8">MFStartup</a>, or the application has already called <a href="https://msdn.microsoft.com/10be2361-b5b4-4c10-92a1-527ca22c74e4">MFShutdown</a>.
              

</td>
</tr>
</table>
 




## -remarks



When you are done using the work queue, call <a href="https://msdn.microsoft.com/bbc22fa7-b4d7-47b2-b065-099fbb2ed092">MFUnlockWorkQueue</a>.




## -see-also




<a href="https://msdn.microsoft.com/b0233589-2a55-4803-9dcb-85d757734dee">MFPutWorkItem</a>



<a href="https://msdn.microsoft.com/67b4f7c6-0d49-4ed0-9bc3-e583451884af">MFPutWorkItemEx</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

