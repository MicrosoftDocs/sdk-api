---
UID: NF:faxcomex._IFaxServerNotify2.OnServerActivityChange
title: _IFaxServerNotify2::OnServerActivityChange (faxcomex.h)
description: The fax service calls the IFaxServerNotify2::OnServerActivityChange method when the fax service activity and status changes.
helpviewer_keywords: ["IFaxServerNotify2 interface [Fax Service]","OnServerActivityChange method","IFaxServerNotify2.OnServerActivityChange","IFaxServerNotify2::OnServerActivityChange","OnServerActivityChange","OnServerActivityChange method [Fax Service]","OnServerActivityChange method [Fax Service]","IFaxServerNotify2 interface","_IFaxServerNotify2.OnServerActivityChange","_IFaxServerNotify2::OnServerActivityChange","_mfax_ifaxservernotify2_onserveractivitychange","fax._mfax_ifaxservernotify2_onserveractivitychange","faxcomex/IFaxServerNotify2::OnServerActivityChange"]
old-location: fax\_mfax_ifaxservernotify2_onserveractivitychange.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_onserveractivitychange.htm
ms.date: 12/05/2018
ms.keywords: IFaxServerNotify2 interface [Fax Service],OnServerActivityChange method, IFaxServerNotify2.OnServerActivityChange, IFaxServerNotify2::OnServerActivityChange, OnServerActivityChange, OnServerActivityChange method [Fax Service], OnServerActivityChange method [Fax Service],IFaxServerNotify2 interface, _IFaxServerNotify2.OnServerActivityChange, _IFaxServerNotify2::OnServerActivityChange, _mfax_ifaxservernotify2_onserveractivitychange, fax._mfax_ifaxservernotify2_onserveractivitychange, faxcomex/IFaxServerNotify2::OnServerActivityChange
f1_keywords:
- faxcomex/IFaxServerNotify2.OnServerActivityChange
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
- IFaxServerNotify2.OnServerActivityChange
- IFaxServerNotify2.OnServerActivityChange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# _IFaxServerNotify2::OnServerActivityChange


## -description


The fax service calls the <b>IFaxServerNotify2::OnServerActivityChange</b> method when the fax service activity and status changes.


## -parameters




### -param pFaxServer

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a>*</b>

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> object.


### -param lIncomingMessages

Type: <b>long</b>

Long value that indicates the total number of incoming fax jobs that the fax service is currently receiving.


### -param lRoutingMessages

Type: <b>long</b>

Long value that indicates the total number of incoming fax jobs that the fax service is currently routing.


### -param lOutgoingMessages

Type: <b>long</b>

Long value that indicates the total number of incoming fax jobs that the fax service is currently sending.


### -param lQueuedMessages

Type: <b>long</b>

Long value that indicates the total number of fax jobs in the fax queue. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To implement this functionality in Visual Basic, select and implement the appropriate event procedure. For an example, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-registering-for-fax-events">Registering for Fax Events</a>.




## -see-also




<a href="/windows/win32/api/faxcomex/nn-faxcomex-_ifaxservernotify2">IFaxServerNotify2</a>
 

 

