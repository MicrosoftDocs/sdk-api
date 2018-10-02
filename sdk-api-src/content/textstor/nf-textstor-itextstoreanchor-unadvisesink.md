---
UID: NF:textstor.ITextStoreAnchor.UnadviseSink
title: ITextStoreAnchor::UnadviseSink
author: windows-sdk-content
description: ITextStoreAnchor::UnadviseSink method
old-location: tsf\itextstoreanchor_unadvisesink.htm
tech.root: TSF
ms.assetid: 01ddc659-0ed9-41e9-bde9-92aad9d74716
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],UnadviseSink method, ITextStoreAnchor.UnadviseSink, ITextStoreAnchor::UnadviseSink, UnadviseSink, UnadviseSink method [Text Services Framework], UnadviseSink method [Text Services Framework],ITextStoreAnchor interface, textstor/ITextStoreAnchor::UnadviseSink, tsf.itextstoreanchor_unadvisesink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
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
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreAnchor.UnadviseSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreAnchor::UnadviseSink


## -description




## -parameters




### -param punk [in]

Pointer to a sink object. Cannot be <b>NULL</b>.


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
<dt><b>CONNECT_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
There is no active sink object.

</td>
</tr>
</table>
 




## -remarks



Every call to the <a href="https://msdn.microsoft.com/a2196d1c-b03e-44b4-b695-970feddb8ce5">ITextStoreAnchor::AdviseSink</a> method, which registers a new sink object, should be matched by a call to this method. If AdviseSink has only updated the <i>dwMask</i> parameter of a sink which was previously registered, a call to <b>UnadviseSink</b> is not required.

For example, to register a sink object, an application calls the <b>AdviseSink</b> method the first time. The application can then call the <b>AdviseSink</b> method again with the same sink object to change the <i>dwMask</i> parameter. To unregister the sink object, an application calls the <b>UnadviseSink</b> method.

The <i>punk</i> parameter must have the same COM identity as the pointer originally passed in the <b>AdviseSink</b> method.




## -see-also




<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a>



<a href="https://msdn.microsoft.com/a2196d1c-b03e-44b4-b695-970feddb8ce5">ITextStoreAnchor::AdviseSink
      </a>
 

 

