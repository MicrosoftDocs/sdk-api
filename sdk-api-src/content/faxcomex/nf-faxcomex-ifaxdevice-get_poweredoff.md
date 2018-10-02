---
UID: NF:faxcomex.IFaxDevice.get_PoweredOff
title: IFaxDevice::get_PoweredOff
author: windows-sdk-content
description: The IFaxDevice::get_PoweredOff property is a Boolean value that indicates whether the fax device is currently available for sending and receiving faxes.
old-location: fax\_mfax_faxdevice_cpp_mfax_faxdevice_poweredoff_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_2fdy.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFaxDevice interface [Fax Service],PoweredOff property, IFaxDevice.PoweredOff, IFaxDevice.get_PoweredOff, IFaxDevice::PoweredOff, IFaxDevice::get_PoweredOff, PoweredOff property [Fax Service], PoweredOff property [Fax Service],IFaxDevice interface, _mfax_faxdevice.poweredoff, fax._mfax_faxdevice_cpp_mfax_faxdevice_poweredoff_cpp, fax._mfax_faxdevice_poweredoff, faxcomex/IFaxDevice::PoweredOff, faxcomex/IFaxDevice::get_PoweredOff, get_PoweredOff
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
 - IFaxDevice.PoweredOff
 - IFaxDevice.get_PoweredOff
 - IFaxDevice.get_PoweredOff
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDevice::get_PoweredOff


## -description


The <b>IFaxDevice::get_PoweredOff</b> property is a Boolean value that indicates whether the fax device is currently available for sending and receiving faxes.

This property is read-only.


## -parameters


## -remarks



If this property is equal to <b>TRUE</b>, the fax device is currently offline and unavailable for sending and receiving faxes. If this property is equal to <b>FALSE</b>, the fax device is online and available.

<div class="alert"><b>Note</b>  The value of this property is set at the time that the <a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a> object is created and is refreshed when you call the <a href="https://msdn.microsoft.com/9517a067-d29b-4362-a3ca-0658498aba5e">IFaxDevice::Refresh</a> method.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a>



<a href="https://msdn.microsoft.com/3f4f4e83-df62-43af-903c-0b816bade3b9">IFaxDevice</a>



<a href="https://msdn.microsoft.com/8e0d5b13-2126-49a2-80b7-ae3a817496bd">Visual Basic Example</a>
 

 

