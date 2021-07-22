---
UID: NF:faxcomex._IFaxServerNotify2.OnDeviceStatusChange
title: _IFaxServerNotify2::OnDeviceStatusChange (faxcomex.h)
description: The fax service calls the IFaxServerNotify2::OnDeviceStatusChange method when there is a change to a fax device status.
helpviewer_keywords: ["IFaxServerNotify2 interface [Fax Service]","OnDeviceStatusChange method","IFaxServerNotify2.OnDeviceStatusChange","IFaxServerNotify2::OnDeviceStatusChange","OnDeviceStatusChange","OnDeviceStatusChange method [Fax Service]","OnDeviceStatusChange method [Fax Service]","IFaxServerNotify2 interface","_IFaxServerNotify2.OnDeviceStatusChange","_IFaxServerNotify2::OnDeviceStatusChange","_mfax_ifaxservernotify2_ondevicestatuschange","fax._mfax_ifaxservernotify2_ondevicestatuschange","faxcomex/IFaxServerNotify2::OnDeviceStatusChange"]
old-location: fax\_mfax_ifaxservernotify2_ondevicestatuschange.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_ondevicestatuschange.htm
ms.date: 12/05/2018
ms.keywords: IFaxServerNotify2 interface [Fax Service],OnDeviceStatusChange method, IFaxServerNotify2.OnDeviceStatusChange, IFaxServerNotify2::OnDeviceStatusChange, OnDeviceStatusChange, OnDeviceStatusChange method [Fax Service], OnDeviceStatusChange method [Fax Service],IFaxServerNotify2 interface, _IFaxServerNotify2.OnDeviceStatusChange, _IFaxServerNotify2::OnDeviceStatusChange, _mfax_ifaxservernotify2_ondevicestatuschange, fax._mfax_ifaxservernotify2_ondevicestatuschange, faxcomex/IFaxServerNotify2::OnDeviceStatusChange
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
 - _IFaxServerNotify2::OnDeviceStatusChange
 - faxcomex/_IFaxServerNotify2::OnDeviceStatusChange
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
 - IFaxServerNotify2.OnDeviceStatusChange
 - IFaxServerNotify2.OnDeviceStatusChange
---

# _IFaxServerNotify2::OnDeviceStatusChange


## -description

The fax service calls the <b>IFaxServerNotify2::OnDeviceStatusChange</b> method when there is a change to a fax device status.

## -parameters

### -param pFaxServer

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a>*</b>

A <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> object.

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

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To implement this functionality in Visual Basic, select and implement the appropriate event procedure. For an example, see <a href="/previous-versions/windows/desktop/fax/-mfax-registering-for-fax-events">Registering for Fax Events</a>.

## -see-also

<a href="/windows/win32/api/faxcomex/nn-faxcomex-_ifaxservernotify2">IFaxServerNotify2</a>