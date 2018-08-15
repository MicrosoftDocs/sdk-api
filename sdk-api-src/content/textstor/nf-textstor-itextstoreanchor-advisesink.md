---
UID: NF:textstor.ITextStoreAnchor.AdviseSink
title: ITextStoreAnchor::AdviseSink
author: windows-sdk-content
description: The ITextStoreAnchor::AdviseSink method installs a new advise sink from the ITextStoreAnchorSink interface or modifies an existing advise sink.
old-location: tsf\itextstoreanchor_advisesink.htm
old-project: TSF
ms.assetid: a2196d1c-b03e-44b4-b695-970feddb8ce5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AdviseSink, AdviseSink method [Text Services Framework], AdviseSink method [Text Services Framework],ITextStoreAnchor interface, ITextStoreAnchor interface [Text Services Framework],AdviseSink method, ITextStoreAnchor.AdviseSink, ITextStoreAnchor::AdviseSink, textstor/ITextStoreAnchor::AdviseSink, tsf.itextstoreanchor_advisesink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textstor.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TsRunType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreAnchor.AdviseSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
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




<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor
      </a>



<a href="https://msdn.microsoft.com/01ddc659-0ed9-41e9-bde9-92aad9d74716">ITextStoreAnchor::UnadviseSink
      </a>



<a href="https://msdn.microsoft.com/8f406b67-f846-4712-b4be-811dbcc6ad55">TS_AS_* Constants
      </a>
 

 

