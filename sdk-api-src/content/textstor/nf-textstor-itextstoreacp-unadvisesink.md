---
UID: NF:textstor.ITextStoreACP.UnadviseSink
title: ITextStoreACP::UnadviseSink (textstor.h)
description: The ITextStoreACP::UnadviseSink method is called by an application to indicate that it no longer requires notifications from the TSF manager. The TSF manager will release the sink interface and stop notifications.
helpviewer_keywords: ["ITextStoreACP interface [Text Services Framework]","UnadviseSink method","ITextStoreACP.UnadviseSink","ITextStoreACP::UnadviseSink","UnadviseSink","UnadviseSink method [Text Services Framework]","UnadviseSink method [Text Services Framework]","ITextStoreACP interface","_tsf_itextstoreacp_unadvisesink_ref","textstor/ITextStoreACP::UnadviseSink","tsf.itextstoreacp_unadvisesink"]
old-location: tsf\itextstoreacp_unadvisesink.htm
tech.root: TSF
ms.assetid: 11445652-e349-46a4-8887-1d1127e16275
ms.date: 12/05/2018
ms.keywords: ITextStoreACP interface [Text Services Framework],UnadviseSink method, ITextStoreACP.UnadviseSink, ITextStoreACP::UnadviseSink, UnadviseSink, UnadviseSink method [Text Services Framework], UnadviseSink method [Text Services Framework],ITextStoreACP interface, _tsf_itextstoreacp_unadvisesink_ref, textstor/ITextStoreACP::UnadviseSink, tsf.itextstoreacp_unadvisesink
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITextStoreACP::UnadviseSink
 - textstor/ITextStoreACP::UnadviseSink
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
 - ITextStoreACP.UnadviseSink
---

# ITextStoreACP::UnadviseSink


## -description

The <b>ITextStoreACP::UnadviseSink</b> method is called by an application to indicate that it no longer requires notifications from the TSF manager. The TSF manager will release the sink interface and stop notifications.

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

Every call to the <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-advisesink">ITextStoreAnchor::AdviseSink</a> method, which registers a new sink object, should be matched by a call to this method. Calls to the <b>ITextStoreAnchor::AdviseSink</b> method that only update the <i>dwMask</i> parameter of a sink which was previously registered, do not require a call to the <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-unadvisesink">ITextStoreAnchor::UnadviseSink</a> method.

For example, to register a sink object, an application calls the <b>ITextStoreAnchor::AdviseSink</b> method the first time. After registering the sink object, the application can call the <b>ITextStoreAnchor::AdviseSink</b> method again with the same sink object to change the <i>dwMask</i> parameter. To unregister the sink object, an application calls the <b>ITextStoreAnchor::UnadviseSink</b> method.

The <i>punk</i> parameter must have the same COM identity as the pointer originally passed in the <b>ITextStoreAnchor::AdviseSink</b> method.

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-advisesink">ITextStoreACP::AdviseSink
      </a>