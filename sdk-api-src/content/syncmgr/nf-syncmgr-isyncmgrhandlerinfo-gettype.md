---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ISyncMgrHandlerInfo::GetType


## -description


Gets the handler type for Sync Center.


## -parameters




### -param pnType [out]

Type: <b><a href="https://msdn.microsoft.com/993a1d55-32ee-4ea7-823f-a533e9646f1f">SYNCMGR_HANDLER_TYPE</a>*</b>

When this method returns, points to a value from the <a href="https://msdn.microsoft.com/993a1d55-32ee-4ea7-823f-a533e9646f1f">SYNCMGR_HANDLER_TYPE</a> enumeration that specifies the handler type. If the method fails, this parameter points to <a href="https://msdn.microsoft.com/993a1d55-32ee-4ea7-823f-a533e9646f1f">SYNCMGR_HT_UNSPECIFIED</a>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. If the method fails, <i>pnType</i> is set to <a href="https://msdn.microsoft.com/993a1d55-32ee-4ea7-823f-a533e9646f1f">SYNCMGR_HT_UNSPECIFIED</a>.




## -remarks



Typically, this value does not change. However, Sync Center calls this method whenever the <a href="https://msdn.microsoft.com/d961aef7-c559-4caa-894e-e86836b142c0">UpdateHandler</a> method is called.


#### Examples




        	The following example shows an implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceHandler::GetType(__out SYNCMGR_HANDLER_TYPE *pnType)
{
    *pnType = SYNCMGR_HT_DEVICE;
    return S_OK;
</pre>
</td>
</tr>
</table></span></div>


