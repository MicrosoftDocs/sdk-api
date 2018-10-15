---
UID: NF:rtworkq.IRtwqAsyncCallback.GetParameters
title: IRtwqAsyncCallback::GetParameters
author: windows-sdk-content
description: Provides configuration information to the dispatching thread for a callback.
old-location: base\irtwqasynccallback_getparameters.htm
tech.root: ProcThread
ms.assetid: C6569BC4-E722-418E-B469-B20877F44648
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetParameters, GetParameters method, GetParameters method,IRtwqAsyncCallback interface, IRtwqAsyncCallback interface,GetParameters method, IRtwqAsyncCallback.GetParameters, IRtwqAsyncCallback::GetParameters, Zero, base.irtwqasynccallback_getparameters, rtworkq/IRtwqAsyncCallback::GetParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rtworkq.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTWorkQ.dll
api_name:
 - IRtwqAsyncCallback.GetParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRtwqAsyncCallback::GetParameters


## -description



Provides configuration information to the dispatching thread for a callback.




## -parameters




### -param pdwFlags [out]

Receives a flag indicating the behavior of the callback object's <a href="https://msdn.microsoft.com/1798C338-4C82-42A7-AE15-ADFD356604BD">IRtwqAsyncCallback::Invoke</a> method. The following values are defined. The default value is zero.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Zero"></a><a id="zero"></a><a id="ZERO"></a><dl>
<dt><b>Zero</b></dt>
</dl>
</td>
<td width="60%">
The callback does not take a long time to complete, but has no specific restrictions on what system calls it makes. The callback generally takes less than 30 milliseconds to complete.

</td>
</tr>
</table>
 


### -param pdwQueue [out]

Receives the identifier of the work queue on which the callback is dispatched. 
          


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_NOTIMPL</b></b></dt>
</dl>
</td>
<td width="60%">
Not implemented. Assume the default behavior.
              

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/E595C072-98F8-4231-9C8F-A8393D751DE6">IRtwqAsyncCallback</a>
 

 

