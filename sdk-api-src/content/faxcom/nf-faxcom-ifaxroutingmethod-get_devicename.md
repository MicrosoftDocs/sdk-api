---
UID: NF:faxcom.IFaxRoutingMethod.get_DeviceName
title: IFaxRoutingMethod::get_DeviceName (faxcom.h)
description: The IFaxRoutingMethod::get_DeviceName property is a null-terminated string that contains the user-friendly display name for a fax port.
helpviewer_keywords: ["DeviceName property [Fax Service]","DeviceName property [Fax Service]","IFaxRoutingMethod interface","IFaxRoutingMethod interface [Fax Service]","DeviceName property","IFaxRoutingMethod.DeviceName","IFaxRoutingMethod.get_DeviceName","IFaxRoutingMethod::DeviceName","IFaxRoutingMethod::get_DeviceName","_mfax_ifaxroutingmethod_get_devicename","fax._mfax_ifaxroutingmethod_get_devicename","fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_devicename_cpp","faxcom/IFaxRoutingMethod::DeviceName","faxcom/IFaxRoutingMethod::get_DeviceName","get_DeviceName"]
old-location: fax\_mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_devicename_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0tk5.htm
ms.date: 12/05/2018
ms.keywords: DeviceName property [Fax Service], DeviceName property [Fax Service],IFaxRoutingMethod interface, IFaxRoutingMethod interface [Fax Service],DeviceName property, IFaxRoutingMethod.DeviceName, IFaxRoutingMethod.get_DeviceName, IFaxRoutingMethod::DeviceName, IFaxRoutingMethod::get_DeviceName, _mfax_ifaxroutingmethod_get_devicename, fax._mfax_ifaxroutingmethod_get_devicename, fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_devicename_cpp, faxcom/IFaxRoutingMethod::DeviceName, faxcom/IFaxRoutingMethod::get_DeviceName, get_DeviceName
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
 - IFaxRoutingMethod::get_DeviceName
 - faxcom/IFaxRoutingMethod::get_DeviceName
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
 - IFaxRoutingMethod.DeviceName
 - IFaxRoutingMethod.get_DeviceName
---

# IFaxRoutingMethod::get_DeviceName


## -description

The <b>IFaxRoutingMethod::get_DeviceName</b> property is a null-terminated string that contains the user-friendly display name for a fax port. 

This property is read-only.

## -parameters

## -remarks

Note that it is possible for multiple fax ports to have the same user-friendly name. You can use the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxroutingmethod-get-deviceid-vb">IFaxRoutingMethod::get_DeviceId</a> property to uniquely identify a fax port.

<b>IFaxRoutingMethod::get_DeviceName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethod">IFaxRoutingMethod</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxroutingmethod-get-deviceid-vb">IFaxRoutingMethod::get_DeviceId</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethods">IFaxRoutingMethods</a>