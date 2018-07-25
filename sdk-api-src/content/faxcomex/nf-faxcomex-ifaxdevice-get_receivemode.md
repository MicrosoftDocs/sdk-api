---
UID: NF:faxcomex.IFaxDevice.get_ReceiveMode
title: IFaxDevice::get_ReceiveMode
author: windows-sdk-content
description: The ReceiveMode property is a value from the FAX_DEVICE_RECEIVE_MODE_ENUM enumeration that defines the way a device answers an incoming call.
old-location: fax\_mfax_faxdevice_receivemode.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_086d.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: FaxDevice object [Fax Service],ReceiveMode property, FaxDevice.ReceiveMode, IFaxDevice.get_ReceiveMode, IFaxDevice.put_ReceiveMode, IFaxDevice::get_ReceiveMode, ReceiveMode property [Fax Service], ReceiveMode property [Fax Service],FaxDevice object, _mfax_faxdevice.receivemode, fax._mfax_faxdevice_receivemode, get_ReceiveMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - FaxDevice.ReceiveMode
 - IFaxDevice.get_ReceiveMode
 - IFaxDevice.put_ReceiveMode
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDevice::get_ReceiveMode


## -description


The <b>ReceiveMode</b> property is a value from the <a href="https://msdn.microsoft.com/library/ms689547(v=VS.85).aspx">FAX_DEVICE_RECEIVE_MODE_ENUM</a> enumeration that defines the way a device answers an incoming call. The value assigned to this property indicates whether the device does not answer the call, the device can answer the call manually, or the device answers the call automatically.

This property is read/write.


## -parameters


## -remarks



You can set only one device to receive faxes manually at any given time. If you set a device to answer manually and another device is already set to the manual mode, the device that had been previously set will automatically change to the no-answer mode. You should call the <a href="https://msdn.microsoft.com/library/ms686727(v=VS.85).aspx">Refresh</a> method on that device to see the change.

Some devices, such as virtual devices, do not support the manual-answer receive mode. For those devices, the <b>ReceiveMode</b> will fail if you set the receive mode to <a href="https://msdn.microsoft.com/library/ms689547(v=VS.85).aspx">fdrmMANUAL_ANSWER</a>. In C++, the method will return an ERROR_NOT_SUPPORTED error code in an <b>Long</b> format.




## -see-also




<a href="https://msdn.microsoft.com/library/ms686192(v=VS.85).aspx">FaxDevice</a>



<a href="https://msdn.microsoft.com/library/ms686193(v=VS.85).aspx">IFaxDevice</a>



<a href="https://msdn.microsoft.com/library/ms693400(v=VS.85).aspx">Visual Basic Example</a>
 

 

