---
UID: NF:faxcomex.IFaxDevice.get_SendingNow
title: IFaxDevice::get_SendingNow
author: windows-sdk-content
description: The IFaxDevice::get_SendingNow property is a Boolean value that indicates whether the fax device is sending a fax at the moment the property is retrieved (the status could change immediately thereafter).
old-location: fax\_mfax_faxdevice_cpp_mfax_faxdevice_sendingnow_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_3vzr.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxDevice interface [Fax Service],SendingNow property, IFaxDevice.SendingNow, IFaxDevice.get_SendingNow, IFaxDevice::SendingNow, IFaxDevice::get_SendingNow, SendingNow property [Fax Service], SendingNow property [Fax Service],IFaxDevice interface, _mfax_faxdevice.sendingnow, fax._mfax_faxdevice_cpp_mfax_faxdevice_sendingnow_cpp, fax._mfax_faxdevice_sendingnow, faxcomex/IFaxDevice::SendingNow, faxcomex/IFaxDevice::get_SendingNow, get_SendingNow
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
 - IFaxDevice.SendingNow
 - IFaxDevice.get_SendingNow
 - IFaxDevice.get_SendingNow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDevice::get_SendingNow


## -description


The <b>IFaxDevice::get_SendingNow</b> property is a Boolean value that indicates whether the fax device is sending a fax at the moment the property is retrieved (the status could change immediately thereafter). 

            
<div class="alert"><b>Note</b>  The value of this property is set at the time that the <a href="https://msdn.microsoft.com/en-us/library/ms686192(v=VS.85).aspx">FaxDevice</a> object is created and is refreshed when you call the <a href="https://msdn.microsoft.com/en-us/library/ms686727(v=VS.85).aspx">IFaxDevice::Refresh</a> method.</div><div> </div>This property is read-only.


## -parameters


## -remarks



If this property is equal to <b>TRUE</b>, the fax device is currently sending a fax. If this property is equal to <b>FALSE</b>, the fax device is not currently sending a fax.

<div class="alert"><b>Note</b>  The value of this property is set at the time that the <a href="https://msdn.microsoft.com/en-us/library/ms686192(v=VS.85).aspx">FaxDevice</a> object is created and is refreshed when you call the <a href="https://msdn.microsoft.com/en-us/library/ms686727(v=VS.85).aspx">IFaxDevice::Refresh</a> method.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686192(v=VS.85).aspx">FaxDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/ms686193(v=VS.85).aspx">IFaxDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692985(v=VS.85).aspx">Visual Basic Example</a>
 

 

