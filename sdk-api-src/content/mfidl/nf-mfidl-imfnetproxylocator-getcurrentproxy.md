---
UID: NF:mfidl.IMFNetProxyLocator.GetCurrentProxy
title: IMFNetProxyLocator::GetCurrentProxy
author: windows-sdk-content
description: Retrieves the current proxy information including hostname and port.
old-location: mf\imfnetproxylocator_getcurrentproxy.htm
tech.root: medfound
ms.assetid: 5bc9a87b-a6d5-4ae0-a3a2-9cef2df79272
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 5bc9a87b-a6d5-4ae0-a3a2-9cef2df79272, GetCurrentProxy, GetCurrentProxy method [Media Foundation], GetCurrentProxy method [Media Foundation],IMFNetProxyLocator interface, IMFNetProxyLocator interface [Media Foundation],GetCurrentProxy method, IMFNetProxyLocator.GetCurrentProxy, IMFNetProxyLocator::GetCurrentProxy, mf.imfnetproxylocator_getcurrentproxy, mfidl/IMFNetProxyLocator::GetCurrentProxy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFNetProxyLocator.GetCurrentProxy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFNetProxyLocator::GetCurrentProxy


## -description



Retrieves the current proxy information including hostname and port.




## -parameters




### -param pszStr [out]

Pointer to a buffer that receives a null-terminated string containing the proxy hostname and port. This parameter can be <b>NULL</b>.


### -param pcchStr [in, out]

On input, specifies the number of elements in the <i>pszStr</i> array. On output, receives the required size of the buffer.


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
<dt><b>E_NOT_SUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer specified in <i>pszStr</i> is too small.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2906b998-f1ca-4c65-b810-cbc360390653">IMFNetProxyLocator</a>
 

 

