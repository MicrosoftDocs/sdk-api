---
UID: NF:faxcom.IFaxPort.get_CanModify
title: IFaxPort::get_CanModify (faxcom.h)
description: The IFaxPort::get_CanModify property is a Boolean value that indicates whether the user has permission to modify configuration information for the fax port.
helpviewer_keywords: ["CanModify property [Fax Service]","CanModify property [Fax Service]","IFaxPort interface","IFaxPort interface [Fax Service]","CanModify property","IFaxPort.CanModify","IFaxPort.get_CanModify","IFaxPort::CanModify","IFaxPort::get_CanModify","_mfax_ifaxport_get_canmodify","fax._mfax_ifaxport_get_canmodify","fax._mfax_ifaxport_mfax_ifaxport_get_canmodify_cpp","faxcom/IFaxPort::CanModify","faxcom/IFaxPort::get_CanModify","get_CanModify"]
old-location: fax\_mfax_ifaxport_mfax_ifaxport_get_canmodify_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_920p.htm
ms.date: 12/05/2018
ms.keywords: CanModify property [Fax Service], CanModify property [Fax Service],IFaxPort interface, IFaxPort interface [Fax Service],CanModify property, IFaxPort.CanModify, IFaxPort.get_CanModify, IFaxPort::CanModify, IFaxPort::get_CanModify, _mfax_ifaxport_get_canmodify, fax._mfax_ifaxport_get_canmodify, fax._mfax_ifaxport_mfax_ifaxport_get_canmodify_cpp, faxcom/IFaxPort::CanModify, faxcom/IFaxPort::get_CanModify, get_CanModify
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
 - IFaxPort::get_CanModify
 - faxcom/IFaxPort::get_CanModify
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
 - IFaxPort.CanModify
 - IFaxPort.get_CanModify
---

# IFaxPort::get_CanModify


## -description

The <b>IFaxPort::get_CanModify</b> property is a Boolean value that indicates whether the user has permission to modify configuration information for the fax port.

This property is read-only.

## -parameters

## -remarks

To ensure that the client has permission to modify the specified fax port, a fax client application can call the <b>IFaxPort::get_CanModify</b> property before calling any method that begins with <b>IFaxPort::put_</b>. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-device-management">Fax Device Management</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>