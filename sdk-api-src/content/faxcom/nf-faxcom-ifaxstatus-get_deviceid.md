---
UID: NF:faxcom.IFaxStatus.get_DeviceId
title: IFaxStatus::get_DeviceId (faxcom.h)
description: Retrieves the DeviceId property for the FaxStatus object of a parent FaxPort object. The DeviceId property is a number representing the permanent line identifier for the fax port.
helpviewer_keywords: ["DeviceId property [Fax Service]","DeviceId property [Fax Service]","IFaxStatus interface","IFaxStatus interface [Fax Service]","DeviceId property","IFaxStatus.DeviceId","IFaxStatus.get_DeviceId","IFaxStatus::DeviceId","IFaxStatus::get_DeviceId","_mfax_ifaxstatus_get_deviceid","fax._mfax_ifaxstatus_get_deviceid","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_deviceid_cpp","faxcom/IFaxStatus::DeviceId","faxcom/IFaxStatus::get_DeviceId","get_DeviceId"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_deviceid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_097o.htm
ms.date: 12/05/2018
ms.keywords: DeviceId property [Fax Service], DeviceId property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],DeviceId property, IFaxStatus.DeviceId, IFaxStatus.get_DeviceId, IFaxStatus::DeviceId, IFaxStatus::get_DeviceId, _mfax_ifaxstatus_get_deviceid, fax._mfax_ifaxstatus_get_deviceid, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_deviceid_cpp, faxcom/IFaxStatus::DeviceId, faxcom/IFaxStatus::get_DeviceId, get_DeviceId
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
 - IFaxStatus::get_DeviceId
 - faxcom/IFaxStatus::get_DeviceId
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
 - IFaxStatus.DeviceId
 - IFaxStatus.get_DeviceId
---

# IFaxStatus::get_DeviceId


## -description

Retrieves the <b>DeviceId</b> property for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>DeviceId</b> property is a number representing the permanent line identifier for the fax port.

This property is read-only.

## -parameters

## -remarks

It is possible for multiple fax ports to have the same user-friendly name. You can use the <b>DeviceId</b> property to uniquely identify a fax port, and thereby associate a <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object with a <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>