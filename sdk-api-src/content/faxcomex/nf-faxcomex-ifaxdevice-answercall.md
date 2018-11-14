---
UID: NF:faxcomex.IFaxDevice.AnswerCall
title: IFaxDevice::AnswerCall
author: windows-sdk-content
description: The IFaxDevice::AnswerCall method causes the fax device to answer an incoming call.
old-location: fax\_mfax_faxdevice_cpp_mfax_faxdevice_answercall_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_76uk.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: AnswerCall, AnswerCall method [Fax Service], AnswerCall method [Fax Service],IFaxDevice interface, IFaxDevice interface [Fax Service],AnswerCall method, IFaxDevice.AnswerCall, IFaxDevice::AnswerCall, _mfax_faxdevice.answercall, fax._mfax_faxdevice_answercall, fax._mfax_faxdevice_cpp_mfax_faxdevice_answercall_cpp, faxcomex/IFaxDevice::AnswerCall
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
 - IFaxDevice.AnswerCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcomex.h
: 
- IFaxDevice.AnswerCall
: 
---

# IFaxDevice::AnswerCall


## -description


The <b>IFaxDevice::AnswerCall</b> method causes the fax device to answer an incoming call.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>IFaxDevice::AnswerCall</b> method will only work on a fax device on the local server. The method will work regardless of the value of the <a href="https://msdn.microsoft.com/en-us/library/ms684558(v=VS.85).aspx">ReceiveMode</a> property.

You can use this method to manually answer a call. You may use this method if the <a href="https://msdn.microsoft.com/en-us/library/ms684558(v=VS.85).aspx">ReceiveMode</a> property is set to answer manually, automatically, or not at all. The fax device must be idle for the incoming call to succeed.

To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_IN_ARCHIVE</a> access right.

If the method succeeds, the service has successfully accepted the request and has validated the parameters and the access rights. Method success does not indicate that the service answered the call and started to receive a fax. If the method succeeds but the service fails to answer a call on a device, as in the case when the device does not respond as expected, no notification is sent.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686192(v=VS.85).aspx">FaxDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/ms686193(v=VS.85).aspx">IFaxDevice</a>
 

 

