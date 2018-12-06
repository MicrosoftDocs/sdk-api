---
UID: NF:faxcomex._IFaxServerNotify2.OnOutgoingMessageAdded
title: "_IFaxServerNotify2::OnOutgoingMessageAdded"
author: windows-sdk-content
description: The fax service calls the IFaxServerNotify2::OnOutgoingMessageAdded method when an outgoing message is added to the outbound fax archive.
old-location: fax\_mfax_ifaxservernotify2_onoutgoingmessageadded.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_onoutgoingmessageadded.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxServerNotify2 interface [Fax Service],OnOutgoingMessageAdded method, IFaxServerNotify2.OnOutgoingMessageAdded, IFaxServerNotify2::OnOutgoingMessageAdded, OnOutgoingMessageAdded, OnOutgoingMessageAdded method [Fax Service], OnOutgoingMessageAdded method [Fax Service],IFaxServerNotify2 interface, _IFaxServerNotify2.OnOutgoingMessageAdded, _IFaxServerNotify2::OnOutgoingMessageAdded, _mfax_ifaxservernotify2_onoutgoingmessageadded, fax._mfax_ifaxservernotify2_onoutgoingmessageadded, faxcomex/IFaxServerNotify2::OnOutgoingMessageAdded
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IFaxServerNotify2.OnOutgoingMessageAdded
 - IFaxServerNotify2.OnOutgoingMessageAdded
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _IFaxServerNotify2::OnOutgoingMessageAdded


## -description


The fax service calls the <b>IFaxServerNotify2::OnOutgoingMessageAdded</b> method when an outgoing message is added to the outbound fax archive.


## -parameters




### -param pFaxServer

Type: <b><a href="https://msdn.microsoft.com/1b049d0c-f7dc-4563-8002-4f711f584577">IFaxServer2</a>*</b>

A <a href="https://msdn.microsoft.com/1b049d0c-f7dc-4563-8002-4f711f584577">IFaxServer2</a> object.


### -param bstrMessageId

Type: <b>BSTR</b>

Null-terminated string that contains the ID of the message added to the outbound fax archive.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To implement this functionality in Visual Basic, select and implement the appropriate event procedure. For an example, see <a href="https://msdn.microsoft.com/3a9f42fa-383a-4072-92a6-b59f7940ab04">Registering for Fax Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/ebd959d0-516c-46a0-95cc-78aa49d50cc1">IFaxServerNotify2</a>
 

 

