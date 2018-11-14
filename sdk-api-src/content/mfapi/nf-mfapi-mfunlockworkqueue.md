---
UID: NF:mfapi.MFUnlockWorkQueue
title: MFUnlockWorkQueue function
author: windows-sdk-content
description: Unlocks a work queue.
old-location: mf\mfunlockworkqueue.htm
tech.root: medfound
ms.assetid: bbc22fa7-b4d7-47b2-b065-099fbb2ed092
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: MFUnlockWorkQueue, MFUnlockWorkQueue function [Media Foundation], bbc22fa7-b4d7-47b2-b065-099fbb2ed092, mf.mfunlockworkqueue, mfapi/MFUnlockWorkQueue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - MFUnlockWorkQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MFUnlockWorkQueue
: 
---

# MFUnlockWorkQueue function


## -description



Unlocks a work queue.




## -parameters




### -param dwWorkQueue [in]

Identifier for the work queue to be unlocked. The identifier is returned by the <a href="https://msdn.microsoft.com/8def4375-919c-4619-9484-9ce2708a3886">MFAllocateWorkQueue</a> function.


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
</table>
 




## -remarks



The application must call <b>MFUnlockWorkQueue</b> once for every call to <a href="https://msdn.microsoft.com/8def4375-919c-4619-9484-9ce2708a3886">MFAllocateWorkQueue</a> and then once for every call to <a href="https://msdn.microsoft.com/307a1ec5-e54a-47f6-8ace-3b935081faf8">MFLockWorkQueue</a>.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

