---
UID: NF:faxcomex._IFaxServerNotify2.OnOutgoingArchiveConfigChange
title: "_IFaxServerNotify2::OnOutgoingArchiveConfigChange"
author: windows-sdk-content
description: The fax service calls the IFaxServerNotify2::OnOutgoingArchiveConfigChange method when there is a configuration change related to the outgoing fax archive.
old-location: fax\_mfax_ifaxservernotify2_onoutgoingarchiveconfigchange.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_onoutgoingarchiveconfigchange.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: IFaxServerNotify2 interface [Fax Service],OnOutgoingArchiveConfigChange method, IFaxServerNotify2.OnOutgoingArchiveConfigChange, IFaxServerNotify2::OnOutgoingArchiveConfigChange, OnOutgoingArchiveConfigChange, OnOutgoingArchiveConfigChange method [Fax Service], OnOutgoingArchiveConfigChange method [Fax Service],IFaxServerNotify2 interface, _IFaxServerNotify2.OnOutgoingArchiveConfigChange, _IFaxServerNotify2::OnOutgoingArchiveConfigChange, _mfax_ifaxservernotify2_onoutgoingarchiveconfigchange, fax._mfax_ifaxservernotify2_onoutgoingarchiveconfigchange, faxcomex/IFaxServerNotify2::OnOutgoingArchiveConfigChange
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
 - IFaxServerNotify2.OnOutgoingArchiveConfigChange
 - IFaxServerNotify2.OnOutgoingArchiveConfigChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _IFaxServerNotify2::OnOutgoingArchiveConfigChange


## -description


The fax service calls the <b>IFaxServerNotify2::OnOutgoingArchiveConfigChange</b> method when there is a configuration change related to the outgoing fax archive.


## -parameters




### -param pFaxServer

TBD




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
 

 

