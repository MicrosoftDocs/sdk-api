---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetBalance
title: IMFMediaEngineEx::GetBalance
author: windows-sdk-content
description: Gets the audio balance.
old-location: mf\imfmediaengineex_getbalance.htm
tech.root: medfound
ms.assetid: 57935B52-27BE-47AF-8702-9DF91E1B515D
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetBalance, GetBalance method [Media Foundation], GetBalance method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetBalance method, IMFMediaEngineEx.GetBalance, IMFMediaEngineEx::GetBalance, mf.imfmediaengineex_getbalance, mfmediaengine/IMFMediaEngineEx::GetBalance
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx.GetBalance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineEx::GetBalance


## -description


Gets the audio balance.




## -parameters






## -returns



Returns the balance. The value can be any number in the following range (inclusive).



<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
The left channel is at full volume; the right channel is silent.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The right channel is at full volume; the left channel is silent.


</td>
</tr>
</table>
 

If the value is zero, the left and right channels are at equal volumes. The default value is zero.






## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

