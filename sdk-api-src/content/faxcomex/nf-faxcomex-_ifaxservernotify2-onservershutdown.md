---
UID: NF:faxcomex._IFaxServerNotify2.OnServerShutDown
title: _IFaxServerNotify2::OnServerShutDown (faxcomex.h)
description: The fax service calls the IFaxServerNotify2::OnServerShutDown method when the fax service shuts down.
helpviewer_keywords: ["IFaxServerNotify2 interface [Fax Service]","OnServerShutDown method","IFaxServerNotify2.OnServerShutDown","IFaxServerNotify2::OnServerShutDown","OnServerShutDown","OnServerShutDown method [Fax Service]","OnServerShutDown method [Fax Service]","IFaxServerNotify2 interface","_IFaxServerNotify2.OnServerShutDown","_IFaxServerNotify2::OnServerShutDown","_mfax_ifaxservernotify2_onservershutdown","fax._mfax_ifaxservernotify2_onservershutdown","faxcomex/IFaxServerNotify2::OnServerShutDown"]
old-location: fax\_mfax_ifaxservernotify2_onservershutdown.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_onservershutdown.htm
ms.date: 12/05/2018
ms.keywords: IFaxServerNotify2 interface [Fax Service],OnServerShutDown method, IFaxServerNotify2.OnServerShutDown, IFaxServerNotify2::OnServerShutDown, OnServerShutDown, OnServerShutDown method [Fax Service], OnServerShutDown method [Fax Service],IFaxServerNotify2 interface, _IFaxServerNotify2.OnServerShutDown, _IFaxServerNotify2::OnServerShutDown, _mfax_ifaxservernotify2_onservershutdown, fax._mfax_ifaxservernotify2_onservershutdown, faxcomex/IFaxServerNotify2::OnServerShutDown
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
 - _IFaxServerNotify2::OnServerShutDown
 - faxcomex/_IFaxServerNotify2::OnServerShutDown
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
 - IFaxServerNotify2.OnServerShutDown
 - IFaxServerNotify2.OnServerShutDown
---

# _IFaxServerNotify2::OnServerShutDown


## -description

The fax service calls the <b>IFaxServerNotify2::OnServerShutDown</b> method when the fax service shuts down.

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