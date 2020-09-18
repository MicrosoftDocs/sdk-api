---
UID: NF:faxcom.IFaxStatus.get_Receive
title: IFaxStatus::get_Receive (faxcom.h)
description: Retrieves the Receive property for the FaxStatus object of a parent FaxPort object. The Receive property is a Boolean value that indicates whether a specified fax port is currently receiving a fax.
helpviewer_keywords: ["IFaxStatus interface [Fax Service]","Receive property","IFaxStatus.Receive","IFaxStatus.get_Receive","IFaxStatus::Receive","IFaxStatus::get_Receive","Receive property [Fax Service]","Receive property [Fax Service]","IFaxStatus interface","_mfax_ifaxstatus_get_receive","fax._mfax_ifaxstatus_get_receive","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_receive_cpp","faxcom/IFaxStatus::Receive","faxcom/IFaxStatus::get_Receive","get_Receive"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_receive_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5u1x.htm
ms.date: 12/05/2018
ms.keywords: IFaxStatus interface [Fax Service],Receive property, IFaxStatus.Receive, IFaxStatus.get_Receive, IFaxStatus::Receive, IFaxStatus::get_Receive, Receive property [Fax Service], Receive property [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_get_receive, fax._mfax_ifaxstatus_get_receive, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_receive_cpp, faxcom/IFaxStatus::Receive, faxcom/IFaxStatus::get_Receive, get_Receive
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
 - IFaxStatus::get_Receive
 - faxcom/IFaxStatus::get_Receive
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
 - IFaxStatus.Receive
 - IFaxStatus.get_Receive
---

# IFaxStatus::get_Receive


## -description

Retrieves the <b>Receive</b> property for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>Receive</b> property is a Boolean value that indicates whether a specified fax port is currently receiving a fax.

This property is read-only.

## -parameters

## -remarks

To determine if a specified port is currently sending a fax, you can call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-send-vb">IFaxStatus::get_Send</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-send-vb">IFaxStatus::get_Send</a>