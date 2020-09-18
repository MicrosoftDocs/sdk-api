---
UID: NF:textstor.ITextStoreAnchor.UnadviseSink
title: ITextStoreAnchor::UnadviseSink (textstor.h)
description: ITextStoreAnchor::UnadviseSink method
helpviewer_keywords: ["ITextStoreAnchor interface [Text Services Framework]","UnadviseSink method","ITextStoreAnchor.UnadviseSink","ITextStoreAnchor::UnadviseSink","UnadviseSink","UnadviseSink method [Text Services Framework]","UnadviseSink method [Text Services Framework]","ITextStoreAnchor interface","textstor/ITextStoreAnchor::UnadviseSink","tsf.itextstoreanchor_unadvisesink"]
old-location: tsf\itextstoreanchor_unadvisesink.htm
tech.root: TSF
ms.assetid: 01ddc659-0ed9-41e9-bde9-92aad9d74716
ms.date: 12/05/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],UnadviseSink method, ITextStoreAnchor.UnadviseSink, ITextStoreAnchor::UnadviseSink, UnadviseSink, UnadviseSink method [Text Services Framework], UnadviseSink method [Text Services Framework],ITextStoreAnchor interface, textstor/ITextStoreAnchor::UnadviseSink, tsf.itextstoreanchor_unadvisesink
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITextStoreAnchor::UnadviseSink
 - textstor/ITextStoreAnchor::UnadviseSink
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
 - ITextStoreAnchor.UnadviseSink
---

# ITextStoreAnchor::UnadviseSink


## -description

Called by an application to indicate that it no longer requires notifications from the TSF manager.

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

Every call to the <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-advisesink">ITextStoreAnchor::AdviseSink</a> method, which registers a new sink object, should be matched by a call to this method. If AdviseSink has only updated the <i>dwMask</i> parameter of a sink which was previously registered, a call to <b>UnadviseSink</b> is not required.

For example, to register a sink object, an application calls the <b>AdviseSink</b> method the first time. The application can then call the <b>AdviseSink</b> method again with the same sink object to change the <i>dwMask</i> parameter. To unregister the sink object, an application calls the <b>UnadviseSink</b> method.

The <i>punk</i> parameter must have the same COM identity as the pointer originally passed in the <b>AdviseSink</b> method.

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-advisesink">ITextStoreAnchor::AdviseSink
      </a>