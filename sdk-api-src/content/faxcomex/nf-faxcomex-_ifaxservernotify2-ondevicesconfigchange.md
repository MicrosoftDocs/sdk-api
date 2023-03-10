---
UID: NF:faxcomex._IFaxServerNotify2.OnDevicesConfigChange
title: _IFaxServerNotify2::OnDevicesConfigChange (faxcomex.h)
description: The fax service calls the IFaxServerNotify2::OnDevicesConfigChange method when there is a change to a fax device configuration.
helpviewer_keywords: ["IFaxServerNotify2 interface [Fax Service]","OnDevicesConfigChange method","IFaxServerNotify2.OnDevicesConfigChange","IFaxServerNotify2::OnDevicesConfigChange","OnDevicesConfigChange","OnDevicesConfigChange method [Fax Service]","OnDevicesConfigChange method [Fax Service]","IFaxServerNotify2 interface","_IFaxServerNotify2.OnDevicesConfigChange","_IFaxServerNotify2::OnDevicesConfigChange","_mfax_ifaxservernotify2_ondevicesconfigchange","fax._mfax_ifaxservernotify2_ondevicesconfigchange","faxcomex/IFaxServerNotify2::OnDevicesConfigChange"]
old-location: fax\_mfax_ifaxservernotify2_ondevicesconfigchange.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_ondevicesconfigchange.htm
ms.date: 12/05/2018
ms.keywords: IFaxServerNotify2 interface [Fax Service],OnDevicesConfigChange method, IFaxServerNotify2.OnDevicesConfigChange, IFaxServerNotify2::OnDevicesConfigChange, OnDevicesConfigChange, OnDevicesConfigChange method [Fax Service], OnDevicesConfigChange method [Fax Service],IFaxServerNotify2 interface, _IFaxServerNotify2.OnDevicesConfigChange, _IFaxServerNotify2::OnDevicesConfigChange, _mfax_ifaxservernotify2_ondevicesconfigchange, fax._mfax_ifaxservernotify2_ondevicesconfigchange, faxcomex/IFaxServerNotify2::OnDevicesConfigChange
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
 - _IFaxServerNotify2::OnDevicesConfigChange
 - faxcomex/_IFaxServerNotify2::OnDevicesConfigChange
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
 - IFaxServerNotify2.OnDevicesConfigChange
 - IFaxServerNotify2.OnDevicesConfigChange
---

# _IFaxServerNotify2::OnDevicesConfigChange


## -description

The fax service calls the <b>IFaxServerNotify2::OnDevicesConfigChange</b> method when there is a change to a fax device configuration.

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