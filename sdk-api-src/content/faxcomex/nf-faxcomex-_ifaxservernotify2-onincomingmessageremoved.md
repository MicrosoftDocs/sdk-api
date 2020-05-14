---
UID: NF:faxcomex._IFaxServerNotify2.OnIncomingMessageRemoved
title: _IFaxServerNotify2::OnIncomingMessageRemoved (faxcomex.h)
description: The fax service calls the IFaxServerNotify2::OnIncomingMessageRemoved method when an incoming message is removed from the inbound fax archive.
helpviewer_keywords: ["IFaxServerNotify2 interface [Fax Service]","OnIncomingMessageRemoved method","IFaxServerNotify2.OnIncomingMessageRemoved","IFaxServerNotify2::OnIncomingMessageRemoved","OnIncomingMessageRemoved","OnIncomingMessageRemoved method [Fax Service]","OnIncomingMessageRemoved method [Fax Service]","IFaxServerNotify2 interface","_IFaxServerNotify2.OnIncomingMessageRemoved","_IFaxServerNotify2::OnIncomingMessageRemoved","_mfax_ifaxservernotify2_onincomingmessageremoved","fax._mfax_ifaxservernotify2_onincomingmessageremoved","faxcomex/IFaxServerNotify2::OnIncomingMessageRemoved"]
old-location: fax\_mfax_ifaxservernotify2_onincomingmessageremoved.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_onincomingmessageremoved.htm
ms.date: 12/05/2018
ms.keywords: IFaxServerNotify2 interface [Fax Service],OnIncomingMessageRemoved method, IFaxServerNotify2.OnIncomingMessageRemoved, IFaxServerNotify2::OnIncomingMessageRemoved, OnIncomingMessageRemoved, OnIncomingMessageRemoved method [Fax Service], OnIncomingMessageRemoved method [Fax Service],IFaxServerNotify2 interface, _IFaxServerNotify2.OnIncomingMessageRemoved, _IFaxServerNotify2::OnIncomingMessageRemoved, _mfax_ifaxservernotify2_onincomingmessageremoved, fax._mfax_ifaxservernotify2_onincomingmessageremoved, faxcomex/IFaxServerNotify2::OnIncomingMessageRemoved
f1_keywords:
- faxcomex/IFaxServerNotify2.OnIncomingMessageRemoved
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Fxscomex.dll
api_name:
- IFaxServerNotify2.OnIncomingMessageRemoved
- IFaxServerNotify2.OnIncomingMessageRemoved
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# _IFaxServerNotify2::OnIncomingMessageRemoved


## -description


The fax service calls the <b>IFaxServerNotify2::OnIncomingMessageRemoved</b> method when an incoming message is removed from the inbound fax archive.


## -parameters




### -param pFaxServer

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a>*</b>

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> object.


### -param bstrMessageId

Type: <b>BSTR</b>

Null-terminated string that contains the ID of the message removed from the inbound fax archive.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To implement this functionality in Visual Basic, select and implement the appropriate event procedure. For an example, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-registering-for-fax-events">Registering for Fax Events</a>.




## -see-also




<a href="/windows/win32/api/faxcomex/nn-faxcomex-_ifaxservernotify2">IFaxServerNotify2</a>
 

 

