---
UID: NF:faxcomex._IFaxServerNotify2.OnReceiptOptionsChange
title: _IFaxServerNotify2::OnReceiptOptionsChange (faxcomex.h)
description: The fax service calls the IFaxServerNotify2::OnReceiptOptionsChange method when there is a change that relates to receipt configuration.
helpviewer_keywords: ["IFaxServerNotify2 interface [Fax Service]","OnReceiptOptionsChange method","IFaxServerNotify2.OnReceiptOptionsChange","IFaxServerNotify2::OnReceiptOptionsChange","OnReceiptOptionsChange","OnReceiptOptionsChange method [Fax Service]","OnReceiptOptionsChange method [Fax Service]","IFaxServerNotify2 interface","_IFaxServerNotify2.OnReceiptOptionsChange","_IFaxServerNotify2::OnReceiptOptionsChange","_mfax_ifaxservernotify2_onreceiptoptionschange","fax._mfax_ifaxservernotify2_onreceiptoptionschange","faxcomex/IFaxServerNotify2::OnReceiptOptionsChange"]
old-location: fax\_mfax_ifaxservernotify2_onreceiptoptionschange.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_onreceiptoptionschange.htm
ms.date: 12/05/2018
ms.keywords: IFaxServerNotify2 interface [Fax Service],OnReceiptOptionsChange method, IFaxServerNotify2.OnReceiptOptionsChange, IFaxServerNotify2::OnReceiptOptionsChange, OnReceiptOptionsChange, OnReceiptOptionsChange method [Fax Service], OnReceiptOptionsChange method [Fax Service],IFaxServerNotify2 interface, _IFaxServerNotify2.OnReceiptOptionsChange, _IFaxServerNotify2::OnReceiptOptionsChange, _mfax_ifaxservernotify2_onreceiptoptionschange, fax._mfax_ifaxservernotify2_onreceiptoptionschange, faxcomex/IFaxServerNotify2::OnReceiptOptionsChange
req.header: faxcomex.h
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IFaxServerNotify2::OnReceiptOptionsChange
 - faxcomex/_IFaxServerNotify2::OnReceiptOptionsChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxServerNotify2.OnReceiptOptionsChange
 - IFaxServerNotify2.OnReceiptOptionsChange
---

# _IFaxServerNotify2::OnReceiptOptionsChange


## -description

The fax service calls the <b>IFaxServerNotify2::OnReceiptOptionsChange</b> method when there is a change that relates to receipt configuration.

## -parameters

### -param pFaxServer

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a>*</b>

A <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To implement this functionality in Visual Basic, select and implement the appropriate event procedure. For an example, see <a href="/previous-versions/windows/desktop/fax/-mfax-registering-for-fax-events">Registering for Fax Events</a>.

## -see-also

<a href="/windows/win32/api/faxcomex/nn-faxcomex-_ifaxservernotify2">IFaxServerNotify2</a>