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

# ITextStoreAnchor::AdviseSink


## -description


The <b>ITextStoreAnchor::AdviseSink</b> method installs a new advise sink from the <a href="https://msdn.microsoft.com/fb96b4fb-864f-4f32-bf7c-cf7f199e552a">ITextStoreAnchorSink</a> interface or modifies an existing advise sink.


## -parameters




### -param riid [in]

Specifies the sink interface. The only supported value is IID_ITextStoreAnchorSink.


### -param punk [in]

Pointer to the sink interface to advise. Cannot be <b>NULL</b>.


### -param dwMask [in]

Specifies the events that notify the advise sink. For more information about possible parameter values, see <a href="https://msdn.microsoft.com/8f406b67-f846-4712-b4be-811dbcc6ad55">TS_AS_* Constants</a>.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The specified sink interface <i>riid</i> could not be obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified sink interface is unsupported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The specified sink object could not be obtained.

</td>
</tr>
</table>
 




## -remarks



Subsequent calls with the same interface, represented by the <i>punk</i> parameter, are handled as requests to update the <i>dwMask</i> parameter. Servers should not call the <b>AddRef</b> method on the sink in response to such a request.

Servers only maintain a single connection point. Attempts to advise a second sink object fail until the original sink object is removed. Applications should use the <a href="https://msdn.microsoft.com/01ddc659-0ed9-41e9-bde9-92aad9d74716">ITextStoreAnchor::UnadviseSink</a> method to unregister the sink object when notifications are not required.




## -see-also




<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">
        ITextStoreAnchor
      </a>



<a href="https://msdn.microsoft.com/01ddc659-0ed9-41e9-bde9-92aad9d74716">
        ITextStoreAnchor::UnadviseSink
      </a>



<a href="https://msdn.microsoft.com/8f406b67-f846-4712-b4be-811dbcc6ad55">TS_AS_* Constants
      </a>
 

 

