---
UID: NF:faxcom.IFaxPort.put_Priority
title: IFaxPort::put_Priority (faxcom.h)
description: The IFaxPort::get_Priority property is a number representing the transmission priority designated for a specified fax port. Priority determines the relative order in which available fax devices send outgoing transmissions. (Put)
helpviewer_keywords: ["IFaxPort interface [Fax Service]","Priority property","IFaxPort.Priority","IFaxPort.put_Priority","IFaxPort::Priority","IFaxPort::get_Priority","IFaxPort::put_Priority","Priority property [Fax Service]","Priority property [Fax Service]","IFaxPort interface","_mfax_ifaxport_get_priority","fax._mfax_ifaxport_get_priority","fax._mfax_ifaxport_mfax_ifaxport_get_priority_cpp","faxcom/IFaxPort::Priority","faxcom/IFaxPort::get_Priority","faxcom/IFaxPort::put_Priority","put_Priority"]
old-location: fax\_mfax_ifaxport_mfax_ifaxport_get_priority_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0515.htm
ms.date: 12/05/2018
ms.keywords: IFaxPort interface [Fax Service],Priority property, IFaxPort.Priority, IFaxPort.put_Priority, IFaxPort::Priority, IFaxPort::get_Priority, IFaxPort::put_Priority, Priority property [Fax Service], Priority property [Fax Service],IFaxPort interface, _mfax_ifaxport_get_priority, fax._mfax_ifaxport_get_priority, fax._mfax_ifaxport_mfax_ifaxport_get_priority_cpp, faxcom/IFaxPort::Priority, faxcom/IFaxPort::get_Priority, faxcom/IFaxPort::put_Priority, put_Priority
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
 - IFaxPort::put_Priority
 - faxcom/IFaxPort::put_Priority
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
 - IFaxPort.Priority
 - IFaxPort.get_Priority
 - IFaxPort.put_Priority
---

# IFaxPort::put_Priority


## -description

The <b>IFaxPort::get_Priority</b> property is a number representing the transmission priority designated for a specified fax port. Priority determines the relative order in which available fax devices send outgoing transmissions.

This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  Before setting a value for this property, a fax client application can call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxport-get-canmodify-vb">IFaxPort::get_CanModify</a> property to ensure that the client has permission to modify configuration information for the specified fax port.</div>
<div> </div>
When the fax server initiates an outgoing fax transmission, it chooses the fax port with the highest priority and send capability. If that port is not available, the server selects the next available port that follows in rank order, and so on. When a client application changes the priority for a fax port, the fax service adjusts the priority for the other fax ports attached to the server. The <b>IFaxPort::get_Priority</b> property has no effect on incoming transmissions.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>
