---
UID: NF:faxcomex._IFaxServerNotify2.OnOutgoingJobChanged
title: "_IFaxServerNotify2::OnOutgoingJobChanged"
author: windows-sdk-content
description: The fax service calls the IFaxServerNotify2::OnOutgoingJobChanged method when the status of an outgoing fax job changes.
old-location: fax\_mfax_ifaxservernotify2_onoutgoingjobchanged.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_onoutgoingjobchanged.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxServerNotify2 interface [Fax Service],OnOutgoingJobChanged method, IFaxServerNotify2.OnOutgoingJobChanged, IFaxServerNotify2::OnOutgoingJobChanged, OnOutgoingJobChanged, OnOutgoingJobChanged method [Fax Service], OnOutgoingJobChanged method [Fax Service],IFaxServerNotify2 interface, _IFaxServerNotify2.OnOutgoingJobChanged, _IFaxServerNotify2::OnOutgoingJobChanged, _mfax_ifaxservernotify2_onoutgoingjobchanged, fax._mfax_ifaxservernotify2_onoutgoingjobchanged, faxcomex/IFaxServerNotify2::OnOutgoingJobChanged
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
 - IFaxServerNotify2.OnOutgoingJobChanged
 - IFaxServerNotify2.OnOutgoingJobChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _IFaxServerNotify2::OnOutgoingJobChanged


## -description


The fax service calls the <b>IFaxServerNotify2::OnOutgoingJobChanged</b> method when the status of an outgoing fax job changes.


## -parameters




### -param pFaxServer

TBD


### -param bstrJobId

Type: <b>BSTR</b>

Null-terminated string that contains the ID of the job for which the status has changed.


### -param pJobStatus

Type: <b><a href="https://msdn.microsoft.com/38527d34-feab-4fae-90c6-45ff9bcfd15c">IFaxJobStatus</a>*</b>

A <a href="https://msdn.microsoft.com/b4e2dc9e-6a32-4fc7-94fc-2132dedcec9e">FaxJobStatus</a> object.


#### - pFaxServer2

Type: <b><a href="https://msdn.microsoft.com/1b049d0c-f7dc-4563-8002-4f711f584577">IFaxServer2</a>*</b>

A <a href="https://msdn.microsoft.com/1b049d0c-f7dc-4563-8002-4f711f584577">IFaxServer2</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To implement this functionality in Visual Basic, select and implement the appropriate event procedure. For an example, see <a href="https://msdn.microsoft.com/3a9f42fa-383a-4072-92a6-b59f7940ab04">Registering for Fax Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/ebd959d0-516c-46a0-95cc-78aa49d50cc1">IFaxServerNotify2</a>
 

 

