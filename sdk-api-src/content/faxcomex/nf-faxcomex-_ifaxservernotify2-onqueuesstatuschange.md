---
UID: NF:faxcomex._IFaxServerNotify2.OnQueuesStatusChange
title: "_IFaxServerNotify2::OnQueuesStatusChange" (faxcomex.h)
author: windows-sdk-content
description: The fax service calls the IFaxServerNotify2::OnQueuesStatusChange method when there is a change in the fax job queue status.
old-location: fax\_mfax_ifaxservernotify2_onqueuesstatuschange.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_onqueuesstatuschange.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxServerNotify2 interface [Fax Service],OnQueuesStatusChange method, IFaxServerNotify2.OnQueuesStatusChange, IFaxServerNotify2::OnQueuesStatusChange, OnQueuesStatusChange, OnQueuesStatusChange method [Fax Service], OnQueuesStatusChange method [Fax Service],IFaxServerNotify2 interface, _IFaxServerNotify2.OnQueuesStatusChange, _IFaxServerNotify2::OnQueuesStatusChange, _mfax_ifaxservernotify2_onqueuesstatuschange, fax._mfax_ifaxservernotify2_onqueuesstatuschange, faxcomex/IFaxServerNotify2::OnQueuesStatusChange
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
 - IFaxServerNotify2.OnQueuesStatusChange
 - IFaxServerNotify2.OnQueuesStatusChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _IFaxServerNotify2::OnQueuesStatusChange


## -description


The fax service calls the <b>IFaxServerNotify2::OnQueuesStatusChange</b> method when there is a change in the fax job queue status.




## -parameters




### -param pFaxServer

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa358976(v=VS.85).aspx">IFaxServer2</a>*</b>

A <a href="https://msdn.microsoft.com/en-us/library/Aa358976(v=VS.85).aspx">IFaxServer2</a> object.


### -param bOutgoingQueueBlocked

Type: <b>VARIANT_BOOL</b>

Specifies a Boolean value that indicates whether the job queue for outgoing faxes is blocked. If this parameter is equal to <b>TRUE</b>, the outgoing job queue is blocked and the fax service is not accepting requests for outgoing fax transmissions. If this parameter is equal to <b>FALSE</b>, the queue is not blocked.


### -param bOutgoingQueuePaused

Type: <b>VARIANT_BOOL</b>

Specifies a Boolean value that indicates whether the job queue for outgoing faxes is paused. If this parameter is equal to <b>TRUE</b>, the job queue is paused and the fax service is not processing jobs in the queue. If this parameter is equal to <b>FALSE</b>, the outgoing queue is not paused.


### -param bIncomingQueueBlocked

Type: <b>VARIANT_BOOL</b>

Specifies a Boolean value that indicates whether the job queue for incoming faxes is blocked. If this parameter is equal to <b>TRUE</b>, the inbound job queue is blocked and the fax service is not answering incoming fax calls. If this parameter is equal to <b>FALSE</b>, the queue is not blocked.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To implement this functionality in Microsoft Visual Basic, select and implement the appropriate event procedure. For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms693013(v=VS.85).aspx">Registering for Fax Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa358971(v=VS.85).aspx">IFaxServerNotify2</a>
 

 

