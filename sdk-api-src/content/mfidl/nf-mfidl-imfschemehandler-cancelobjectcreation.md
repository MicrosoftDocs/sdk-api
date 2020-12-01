---
UID: NF:mfidl.IMFSchemeHandler.CancelObjectCreation
title: IMFSchemeHandler::CancelObjectCreation (mfidl.h)
description: Cancels the current request to create an object from a URL.
helpviewer_keywords: ["662a4c47-95f8-4a84-ab2b-96e51d13906c","CancelObjectCreation","CancelObjectCreation method [Media Foundation]","CancelObjectCreation method [Media Foundation]","IMFSchemeHandler interface","IMFSchemeHandler interface [Media Foundation]","CancelObjectCreation method","IMFSchemeHandler.CancelObjectCreation","IMFSchemeHandler::CancelObjectCreation","mf.imfschemehandler_cancelobjectcreation","mfidl/IMFSchemeHandler::CancelObjectCreation"]
old-location: mf\imfschemehandler_cancelobjectcreation.htm
tech.root: mf
ms.assetid: 662a4c47-95f8-4a84-ab2b-96e51d13906c
ms.date: 12/05/2018
ms.keywords: 662a4c47-95f8-4a84-ab2b-96e51d13906c, CancelObjectCreation, CancelObjectCreation method [Media Foundation], CancelObjectCreation method [Media Foundation],IMFSchemeHandler interface, IMFSchemeHandler interface [Media Foundation],CancelObjectCreation method, IMFSchemeHandler.CancelObjectCreation, IMFSchemeHandler::CancelObjectCreation, mf.imfschemehandler_cancelobjectcreation, mfidl/IMFSchemeHandler::CancelObjectCreation
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSchemeHandler::CancelObjectCreation
 - mfidl/IMFSchemeHandler::CancelObjectCreation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSchemeHandler.CancelObjectCreation
---

# IMFSchemeHandler::CancelObjectCreation


## -description

Cancels the current request to create an object from a URL.

## -parameters

### -param pIUnknownCancelCookie [in]

Pointer to the <b>IUnknown</b> interface that was returned in the <i>ppIUnknownCancelCookie</i> parameter of the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject">IMFSchemeHandler::BeginCreateObject</a> method.

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
</table>

## -remarks

You can use this method to cancel a previous call to <a href="/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject">BeginCreateObject</a>. Because that method is asynchronous, however, it might be completed before the operation can be canceled. Therefore, your callback might still be invoked after you call this method.

The operation cannot be canceled if <a href="/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject">BeginCreateObject</a> returns <b>NULL</b> in the <i>ppIUnknownCancelCookie</i> parameter.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler">IMFSchemeHandler</a>



<a href="/windows/desktop/medfound/scheme-handlers-and-byte-stream-handlers">Scheme Handlers and Byte-Stream Handlers</a>