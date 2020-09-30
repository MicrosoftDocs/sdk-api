---
UID: NF:textstor.ITextStoreACP2.UnadviseSink
title: ITextStoreACP2::UnadviseSink (textstor.h)
description: Called by an application to indicate that it no longer requires notifications from the TSF manager. The TSF manager will release the sink interface and stop notifications.
helpviewer_keywords: ["ITextStoreACP2 interface [Text Services Framework]","UnadviseSink method","ITextStoreACP2.UnadviseSink","ITextStoreACP2::UnadviseSink","UnadviseSink","UnadviseSink method [Text Services Framework]","UnadviseSink method [Text Services Framework]","ITextStoreACP2 interface","textstor/ITextStoreACP2::UnadviseSink","tsf.itextstoreacp2_unadvisesink"]
old-location: tsf\itextstoreacp2_unadvisesink.htm
tech.root: TSF
ms.assetid: 08c78d99-a6ff-4ac1-9357-77bbae70400f
ms.date: 12/05/2018
ms.keywords: ITextStoreACP2 interface [Text Services Framework],UnadviseSink method, ITextStoreACP2.UnadviseSink, ITextStoreACP2::UnadviseSink, UnadviseSink, UnadviseSink method [Text Services Framework], UnadviseSink method [Text Services Framework],ITextStoreACP2 interface, textstor/ITextStoreACP2::UnadviseSink, tsf.itextstoreacp2_unadvisesink
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStoreACP2::UnadviseSink
 - textstor/ITextStoreACP2::UnadviseSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACP2.UnadviseSink
---

# ITextStoreACP2::UnadviseSink


## -description

Called by an application to indicate that it no longer requires notifications from the TSF manager. The TSF manager will release the sink interface and stop notifications.

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

Every call to the <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-advisesink">AdviseSink</a> method, which registers a new sink object, should be matched by a call to this method. Calls to the <b>AdviseSink</b> method that only update the <i>dwMask</i> parameter of a sink which was previously registered, do not require a call to the <b>UnadviseSink</b> method.

For example, to register a sink object, an application calls the <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-advisesink">AdviseSink</a> method the first time. After registering the sink object, the application can call the <b>AdviseSink</b> method again with the same sink object to change the <i>dwMask</i> parameter. To unregister the sink object, an application calls the <b>UnadviseSink</b> method.

The <i>punk</i> parameter must have the same COM identity as the pointer originally passed in the <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-advisesink">AdviseSink</a> method.

## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-advisesink">AdviseSink</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>