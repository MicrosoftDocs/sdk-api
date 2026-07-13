---
UID: NF:faxcomex.IFaxDevice.AnswerCall
title: IFaxDevice::AnswerCall (faxcomex.h)
description: The IFaxDevice::AnswerCall method causes the fax device to answer an incoming call.
helpviewer_keywords: ["AnswerCall","AnswerCall method [Fax Service]","AnswerCall method [Fax Service]","IFaxDevice interface","IFaxDevice interface [Fax Service]","AnswerCall method","IFaxDevice.AnswerCall","IFaxDevice::AnswerCall","_mfax_faxdevice.answercall","fax._mfax_faxdevice_answercall","fax._mfax_faxdevice_cpp_mfax_faxdevice_answercall_cpp","faxcomex/IFaxDevice::AnswerCall"]
old-location: fax\_mfax_faxdevice_cpp_mfax_faxdevice_answercall_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_76uk.htm
ms.date: 12/05/2018
ms.keywords: AnswerCall, AnswerCall method [Fax Service], AnswerCall method [Fax Service],IFaxDevice interface, IFaxDevice interface [Fax Service],AnswerCall method, IFaxDevice.AnswerCall, IFaxDevice::AnswerCall, _mfax_faxdevice.answercall, fax._mfax_faxdevice_answercall, fax._mfax_faxdevice_cpp_mfax_faxdevice_answercall_cpp, faxcomex/IFaxDevice::AnswerCall
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
 - IFaxDevice::AnswerCall
 - faxcomex/IFaxDevice::AnswerCall
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
 - IFaxDevice.AnswerCall
---

# IFaxDevice::AnswerCall


## -description

The <b>IFaxDevice::AnswerCall</b> method causes the fax device to answer an incoming call.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>IFaxDevice::AnswerCall</b> method will only work on a fax device on the local server. The method will work regardless of the value of the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice-receivemode">ReceiveMode</a> property.

You can use this method to manually answer a call. You may use this method if the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice-receivemode">ReceiveMode</a> property is set to answer manually, automatically, or not at all. The fax device must be idle for the incoming call to succeed.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_IN_ARCHIVE</a> access right.

If the method succeeds, the service has successfully accepted the request and has validated the parameters and the access rights. Method success does not indicate that the service answered the call and started to receive a fax. If the method succeeds but the service fails to answer a call on a device, as in the case when the device does not respond as expected, no notification is sent.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice">FaxDevice</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdevice">IFaxDevice</a>
