---
UID: NF:faxcomex.IFaxDevice.put_ReceiveMode
title: IFaxDevice::put_ReceiveMode (faxcomex.h)
description: The ReceiveMode property is a value from the FAX_DEVICE_RECEIVE_MODE_ENUM enumeration that defines the way a device answers an incoming call. (Put)
helpviewer_keywords: ["IFaxDevice interface [Fax Service]","ReceiveMode property","IFaxDevice.ReceiveMode","IFaxDevice.put_ReceiveMode","IFaxDevice::ReceiveMode","IFaxDevice::get_ReceiveMode","IFaxDevice::put_ReceiveMode","ReceiveMode property [Fax Service]","ReceiveMode property [Fax Service]","IFaxDevice interface","_mfax_faxdevice.receivemode_cpp","fax._mfax_faxdevice_receivemode_cpp","faxcomex/IFaxDevice::ReceiveMode","faxcomex/IFaxDevice::get_ReceiveMode","faxcomex/IFaxDevice::put_ReceiveMode","put_ReceiveMode"]
old-location: fax\_mfax_faxdevice_receivemode_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_086d_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxDevice interface [Fax Service],ReceiveMode property, IFaxDevice.ReceiveMode, IFaxDevice.put_ReceiveMode, IFaxDevice::ReceiveMode, IFaxDevice::get_ReceiveMode, IFaxDevice::put_ReceiveMode, ReceiveMode property [Fax Service], ReceiveMode property [Fax Service],IFaxDevice interface, _mfax_faxdevice.receivemode_cpp, fax._mfax_faxdevice_receivemode_cpp, faxcomex/IFaxDevice::ReceiveMode, faxcomex/IFaxDevice::get_ReceiveMode, faxcomex/IFaxDevice::put_ReceiveMode, put_ReceiveMode
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IFaxDevice::put_ReceiveMode
 - faxcomex/IFaxDevice::put_ReceiveMode
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
 - IFaxDevice.ReceiveMode
 - IFaxDevice.get_ReceiveMode
 - IFaxDevice.put_ReceiveMode
---

# IFaxDevice::put_ReceiveMode


## -description

The <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice-receivemode">ReceiveMode</a> property is a value from the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_device_receive_mode_enum">FAX_DEVICE_RECEIVE_MODE_ENUM</a> enumeration that defines the way a device answers an incoming call. The value assigned to this property indicates whether the device does not answer the call, the device can answer the call manually, or the device answers the call automatically.

This property is read/write.

## -parameters

## -remarks

You can set only one device to receive faxes manually at any given time. If you set a device to answer manually and another device is already set to the manual mode, the device that had been previously set will automatically change to the no-answer mode. You should call the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice-refresh-vb">IFaxDevice::Refresh</a> method on that device to see the change.

Some devices, such as virtual devices, do not support the manual-answer receive mode. For those devices, the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice-receivemode">ReceiveMode</a> will fail if you set the receive mode to <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_device_receive_mode_enum">fdrmMANUAL_ANSWER</a>. In C++, the method will return an ERROR_NOT_SUPPORTED error code in an <b>HRESULT</b> format.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice">FaxDevice</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdevice">IFaxDevice</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-configuring-a-fax-device">Visual Basic Example</a>
