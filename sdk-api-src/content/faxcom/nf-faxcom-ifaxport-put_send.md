---
UID: NF:faxcom.IFaxPort.put_Send
title: IFaxPort::put_Send (faxcom.h)
description: The IFaxPort::get_Send property is a Boolean value that indicates whether a fax port is enabled to send faxes. (Put)
helpviewer_keywords: ["IFaxPort interface [Fax Service]","Send property","IFaxPort.Send","IFaxPort.put_Send","IFaxPort::Send","IFaxPort::get_Send","IFaxPort::put_Send","Send property [Fax Service]","Send property [Fax Service]","IFaxPort interface","_mfax_ifaxport_get_send","fax._mfax_ifaxport_get_send","fax._mfax_ifaxport_mfax_ifaxport_get_send_cpp","faxcom/IFaxPort::Send","faxcom/IFaxPort::get_Send","faxcom/IFaxPort::put_Send","put_Send"]
old-location: fax\_mfax_ifaxport_mfax_ifaxport_get_send_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9uqs.htm
ms.date: 12/05/2018
ms.keywords: IFaxPort interface [Fax Service],Send property, IFaxPort.Send, IFaxPort.put_Send, IFaxPort::Send, IFaxPort::get_Send, IFaxPort::put_Send, Send property [Fax Service], Send property [Fax Service],IFaxPort interface, _mfax_ifaxport_get_send, fax._mfax_ifaxport_get_send, fax._mfax_ifaxport_mfax_ifaxport_get_send_cpp, faxcom/IFaxPort::Send, faxcom/IFaxPort::get_Send, faxcom/IFaxPort::put_Send, put_Send
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Faxcom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxPort::put_Send
 - faxcom/IFaxPort::put_Send
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxPort.Send
 - IFaxPort.get_Send
 - IFaxPort.put_Send
---

# IFaxPort::put_Send


## -description

The <b>IFaxPort::get_Send</b> property is a Boolean value that indicates whether a fax port is enabled to send faxes. 

This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  Before setting a value for this property, a fax client application can call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxport-get-canmodify-vb">IFaxPort::get_CanModify</a> property to ensure that the client has permission to modify configuration information for the specified fax port.</div>
<div> </div>
The <b>IFaxPort::get_Send</b> property returns a value of <b>TRUE</b> if the fax port is enabled to send faxes. If a fax client application passes a value of <b>TRUE</b> to the property, it enables the fax port to send faxes.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>
