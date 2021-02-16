---
UID: NF:faxcom.IFaxStatus.get_Send
title: IFaxStatus::get_Send (faxcom.h)
description: Retrieves the Send property for the FaxStatus object of a parent FaxPort object. The Send property is a Boolean value that indicates whether a specified fax port is currently sending a fax.
helpviewer_keywords: ["IFaxStatus interface [Fax Service]","Send property","IFaxStatus.Send","IFaxStatus.get_Send","IFaxStatus::Send","IFaxStatus::get_Send","Send property [Fax Service]","Send property [Fax Service]","IFaxStatus interface","_mfax_ifaxstatus_get_send","fax._mfax_ifaxstatus_get_send","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_send_cpp","faxcom/IFaxStatus::Send","faxcom/IFaxStatus::get_Send","get_Send"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_send_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_58f8.htm
ms.date: 12/05/2018
ms.keywords: IFaxStatus interface [Fax Service],Send property, IFaxStatus.Send, IFaxStatus.get_Send, IFaxStatus::Send, IFaxStatus::get_Send, Send property [Fax Service], Send property [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_get_send, fax._mfax_ifaxstatus_get_send, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_send_cpp, faxcom/IFaxStatus::Send, faxcom/IFaxStatus::get_Send, get_Send
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
 - IFaxStatus::get_Send
 - faxcom/IFaxStatus::get_Send
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
 - IFaxStatus.Send
 - IFaxStatus.get_Send
---

# IFaxStatus::get_Send


## -description

Retrieves the <b>Send</b> property for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>Send</b> property is a Boolean value that indicates whether a specified fax port is currently sending a fax. 

This property is read-only.

## -parameters

## -remarks

You can call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-receive-vb">IFaxStatus::get_Receive</a> method to determine if a specified port is currently receiving a fax.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-receive-vb">IFaxStatus::get_Receive</a>