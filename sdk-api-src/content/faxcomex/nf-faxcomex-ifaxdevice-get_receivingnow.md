---
UID: NF:faxcomex.IFaxDevice.get_ReceivingNow
title: IFaxDevice::get_ReceivingNow
author: windows-sdk-content
description: The IFaxDevice::get_ReceivingNow property is a Boolean value that indicates whether the fax device is receiving a fax at the moment the property is retrieved (the status could change immediately thereafter).
old-location: fax\_mfax_faxdevice_cpp_mfax_faxdevice_receivingnow_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_64on.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxDevice interface [Fax Service],ReceivingNow property, IFaxDevice.ReceivingNow, IFaxDevice.get_ReceivingNow, IFaxDevice.put_ReceivingNow, IFaxDevice::ReceivingNow, IFaxDevice::get_ReceivingNow, IFaxDevice::put_ReceivingNow, ReceivingNow property [Fax Service], ReceivingNow property [Fax Service],IFaxDevice interface, _mfax_faxdevice.receivingnow, fax._mfax_faxdevice_cpp_mfax_faxdevice_receivingnow_cpp, fax._mfax_faxdevice_receivingnow, faxcomex/IFaxDevice::ReceivingNow, faxcomex/IFaxDevice::get_ReceivingNow, faxcomex/IFaxDevice::put_ReceivingNow, get_ReceivingNow
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
 - IFaxDevice.ReceivingNow
 - IFaxDevice.get_ReceivingNow
 - IFaxDevice.put_ReceivingNow
 - IFaxDevice.get_ReceivingNow
 - IFaxDevice.put_ReceivingNow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDevice::get_ReceivingNow


## -description


The <b>IFaxDevice::get_ReceivingNow</b> property is a Boolean value that indicates whether the fax device is receiving a fax at the moment the property is retrieved (the status could change immediately thereafter).

This property is read/write.


## -parameters


## -remarks



If this property is equal to <b>TRUE</b>, the fax device is currently receiving a fax. If this property is equal to <b>FALSE</b>, the fax device is not currently receiving a fax.

<div class="alert"><b>Note</b>  The value of this property is set at the time that the <a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a> object is created and is refreshed when you call the <a href="https://msdn.microsoft.com/9517a067-d29b-4362-a3ca-0658498aba5e">IFaxDevice::Refresh</a> method.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a>



<a href="https://msdn.microsoft.com/3f4f4e83-df62-43af-903c-0b816bade3b9">IFaxDevice</a>



<a href="https://msdn.microsoft.com/8e0d5b13-2126-49a2-80b7-ae3a817496bd">Visual Basic Example</a>
 

 

