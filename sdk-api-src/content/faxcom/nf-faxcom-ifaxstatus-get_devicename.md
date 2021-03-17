---
UID: NF:faxcom.IFaxStatus.get_DeviceName
title: IFaxStatus::get_DeviceName (faxcom.h)
description: Retrieves the DeviceName property for the FaxStatus object of a parent FaxPort object. The DeviceName property is a null-terminated string that contains the user-friendly display name for the fax port.
helpviewer_keywords: ["DeviceName property [Fax Service]","DeviceName property [Fax Service]","IFaxStatus interface","IFaxStatus interface [Fax Service]","DeviceName property","IFaxStatus.DeviceName","IFaxStatus.get_DeviceName","IFaxStatus::DeviceName","IFaxStatus::get_DeviceName","_mfax_ifaxstatus_get_devicename","fax._mfax_ifaxstatus_get_devicename","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_devicename_cpp","faxcom/IFaxStatus::DeviceName","faxcom/IFaxStatus::get_DeviceName","get_DeviceName"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_devicename_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_67mt.htm
ms.date: 12/05/2018
ms.keywords: DeviceName property [Fax Service], DeviceName property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],DeviceName property, IFaxStatus.DeviceName, IFaxStatus.get_DeviceName, IFaxStatus::DeviceName, IFaxStatus::get_DeviceName, _mfax_ifaxstatus_get_devicename, fax._mfax_ifaxstatus_get_devicename, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_devicename_cpp, faxcom/IFaxStatus::DeviceName, faxcom/IFaxStatus::get_DeviceName, get_DeviceName
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
 - IFaxStatus::get_DeviceName
 - faxcom/IFaxStatus::get_DeviceName
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
 - IFaxStatus.DeviceName
 - IFaxStatus.get_DeviceName
---

# IFaxStatus::get_DeviceName


## -description

Retrieves the <b>DeviceName</b> property for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>DeviceName</b> property is a null-terminated string that contains the user-friendly display name for the fax port.

This property is read-only.

## -parameters

## -remarks

Note that it is possible for multiple fax ports to have the same user-friendly name. You can use the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-deviceid-vb">DeviceId</a> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object to uniquely identify a fax port, and associate a FaxStatus object with a <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object.

The <b>IFaxStatus::get_DeviceName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-deviceid-vb">IFaxStatus::get_DeviceId</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>