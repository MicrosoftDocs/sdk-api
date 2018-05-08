---
UID: NF:faxcomex.IFaxDevice.get_ReceiveMode
title: IFaxDevice::get_ReceiveMode
author: windows-driver-content
description: The ReceiveMode property is a value from the FAX_DEVICE_RECEIVE_MODE_ENUM enumeration that defines the way a device answers an incoming call.
old-location: fax\_mfax_faxdevice_receivemode_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_086d_cpp.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFaxDevice interface [Fax Service],ReceiveMode property, IFaxDevice.ReceiveMode, IFaxDevice.get_ReceiveMode, IFaxDevice::ReceiveMode, IFaxDevice::get_ReceiveMode, IFaxDevice::put_ReceiveMode, ReceiveMode property [Fax Service], ReceiveMode property [Fax Service],IFaxDevice interface, _mfax_faxdevice.receivemode_cpp, fax._mfax_faxdevice_receivemode_cpp, faxcomex/IFaxDevice::ReceiveMode, faxcomex/IFaxDevice::get_ReceiveMode, faxcomex/IFaxDevice::put_ReceiveMode, get_ReceiveMode
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxDevice.ReceiveMode
-	IFaxDevice.get_ReceiveMode
-	IFaxDevice.put_ReceiveMode
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDevice::get_ReceiveMode


## -description


The <a href="https://msdn.microsoft.com/d65397eb-2ede-4320-82ea-8fc48aa3f2b0">ReceiveMode</a> property is a value from the <a href="https://msdn.microsoft.com/0fb87bfd-61b0-4130-86fd-0e6579bc55ea">FAX_DEVICE_RECEIVE_MODE_ENUM</a> enumeration that defines the way a device answers an incoming call. The value assigned to this property indicates whether the device does not answer the call, the device can answer the call manually, or the device answers the call automatically.

This property is read/write.


## -parameters


## -remarks



You can set only one device to receive faxes manually at any given time. If you set a device to answer manually and another device is already set to the manual mode, the device that had been previously set will automatically change to the no-answer mode. You should call the <a href="https://msdn.microsoft.com/9517a067-d29b-4362-a3ca-0658498aba5e">IFaxDevice::Refresh</a> method on that device to see the change.

Some devices, such as virtual devices, do not support the manual-answer receive mode. For those devices, the <a href="https://msdn.microsoft.com/d65397eb-2ede-4320-82ea-8fc48aa3f2b0">ReceiveMode</a> will fail if you set the receive mode to <a href="https://msdn.microsoft.com/0fb87bfd-61b0-4130-86fd-0e6579bc55ea">fdrmMANUAL_ANSWER</a>. In C++, the method will return an ERROR_NOT_SUPPORTED error code in an <b>HRESULT</b> format.




## -see-also




<a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a>



<a href="https://msdn.microsoft.com/3f4f4e83-df62-43af-903c-0b816bade3b9">IFaxDevice</a>



<a href="https://msdn.microsoft.com/64bdc08c-1902-448a-9eda-b557ab4bb095">Visual Basic Example</a>
 

 

