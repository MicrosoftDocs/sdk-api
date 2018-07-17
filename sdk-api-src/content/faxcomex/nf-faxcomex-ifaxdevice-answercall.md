---
UID: NF:faxcomex.IFaxDevice.AnswerCall
title: IFaxDevice::AnswerCall
author: windows-sdk-content
description: The AnswerCall method causes the fax device to answer an incoming call.
old-location: fax\_mfax_faxdevice_answercall_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_76uk.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: AnswerCall, AnswerCall method [Fax Service], AnswerCall method [Fax Service],FaxDevice object, FaxDevice object [Fax Service],AnswerCall method, FaxDevice.AnswerCall, IFaxDevice.AnswerCall, IFaxDevice::AnswerCall, _mfax_faxdevice.answercall, fax._mfax_faxdevice_answercall, fax._mfax_faxdevice_answercall_vb
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
 - FaxDevice.AnswerCall
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDevice::AnswerCall


## -description


The <b>AnswerCall</b> method causes the fax device to answer an incoming call.


## -parameters






## -remarks



The <b>AnswerCall</b> method will only work on a fax device on the local server. The method will work regardless of the value of the <a href="https://msdn.microsoft.com/d65397eb-2ede-4320-82ea-8fc48aa3f2b0">ReceiveMode</a> property.

You can use this method to manually answer a call. You may use this method if the <a href="https://msdn.microsoft.com/d65397eb-2ede-4320-82ea-8fc48aa3f2b0">ReceiveMode</a> property is set to answer manually, automatically, or not at all. The fax device must be idle for the incoming call to succeed.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_IN_ARCHIVE</a> access right.

If the method succeeds, the service has successfully accepted the request and has validated the parameters and the access rights. Method success does not indicate that the service answered the call and started to receive a fax. If the method succeeds but the service fails to answer a call on a device, as in the case when the device does not respond as expected, no notification is sent.




## -see-also




<a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a>



<a href="https://msdn.microsoft.com/3f4f4e83-df62-43af-903c-0b816bade3b9">IFaxDevice</a>
 

 

