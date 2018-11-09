---
UID: NF:faxcomex._IFaxServerNotify2.OnDeviceStatusChange
title: "_IFaxServerNotify2::OnDeviceStatusChange"
author: windows-sdk-content
description: The fax service calls the IFaxServerNotify2::OnDeviceStatusChange method when there is a change to a fax device status.
old-location: fax\_mfax_ifaxservernotify2_ondevicestatuschange.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_ondevicestatuschange.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: IFaxServerNotify2 interface [Fax Service],OnDeviceStatusChange method, IFaxServerNotify2.OnDeviceStatusChange, IFaxServerNotify2::OnDeviceStatusChange, OnDeviceStatusChange, OnDeviceStatusChange method [Fax Service], OnDeviceStatusChange method [Fax Service],IFaxServerNotify2 interface, _IFaxServerNotify2.OnDeviceStatusChange, _IFaxServerNotify2::OnDeviceStatusChange, _mfax_ifaxservernotify2_ondevicestatuschange, fax._mfax_ifaxservernotify2_ondevicestatuschange, faxcomex/IFaxServerNotify2::OnDeviceStatusChange
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
 - IFaxServerNotify2.OnDeviceStatusChange
 - IFaxServerNotify2.OnDeviceStatusChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _IFaxServerNotify2::OnDeviceStatusChange


## -description


The fax service calls the <b>IFaxServerNotify2::OnDeviceStatusChange</b> method when there is a change to a fax device status.


## -parameters




### -param pFaxServer

TBD


### -param lDeviceId

Type: <b>long</b>

Long value that contains the ID of the device for which the status has changed.


### -param bPoweredOff

Type: <b>VARIANT_BOOL</b>

Boolean value. If this parameter is equal to <b>TRUE</b>, the fax device is currently offline and unavailable for sending and receiving faxes. If this parameter is equal to <b>FALSE</b>, the fax device is online and available.


### -param bSending

Type: <b>VARIANT_BOOL</b>

Boolean value. If this parameter is equal to <b>TRUE</b>, the fax device is sending faxes. If this parameter is equal to <b>FALSE</b>, the fax device is not sending faxes.


### -param bReceiving

Type: <b>VARIANT_BOOL</b>

Boolean value. If this parameter is equal to <b>TRUE</b>, the fax device is receiving faxes. If this parameter is equal to <b>FALSE</b>, the fax device is not receiving faxes. 


### -param bRinging

Type: <b>VARIANT_BOOL</b>

Boolean value. If this parameter is equal to <b>TRUE</b>, the fax device is ringing. If this parameter is equal to <b>FALSE</b>, the fax device is not ringing.


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
 

 

