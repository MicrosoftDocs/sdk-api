---
UID: NF:faxcom.IFaxPort.get_Name
title: IFaxPort::get_Name (faxcom.h)
description: The IFaxPort::get_Name property is a null-terminated string that contains the user-friendly display name for a fax port.
helpviewer_keywords: ["IFaxPort interface [Fax Service]","Name property","IFaxPort.Name","IFaxPort.get_Name","IFaxPort::Name","IFaxPort::get_Name","Name property [Fax Service]","Name property [Fax Service]","IFaxPort interface","_mfax_ifaxport_get_name","fax._mfax_ifaxport_get_name","fax._mfax_ifaxport_mfax_ifaxport_get_name_cpp","faxcom/IFaxPort::Name","faxcom/IFaxPort::get_Name","get_Name"]
old-location: fax\_mfax_ifaxport_mfax_ifaxport_get_name_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1ep1.htm
ms.date: 12/05/2018
ms.keywords: IFaxPort interface [Fax Service],Name property, IFaxPort.Name, IFaxPort.get_Name, IFaxPort::Name, IFaxPort::get_Name, Name property [Fax Service], Name property [Fax Service],IFaxPort interface, _mfax_ifaxport_get_name, fax._mfax_ifaxport_get_name, fax._mfax_ifaxport_mfax_ifaxport_get_name_cpp, faxcom/IFaxPort::Name, faxcom/IFaxPort::get_Name, get_Name
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
 - IFaxPort::get_Name
 - faxcom/IFaxPort::get_Name
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
 - IFaxPort.Name
 - IFaxPort.get_Name
---

# IFaxPort::get_Name


## -description

The <b>IFaxPort::get_Name</b> property is a null-terminated string that contains the 
user-friendly display name for a fax port.

This property is read-only.

## -parameters

## -remarks

Note that it is possible for multiple fax ports to have the same user-friendly 
name. Use the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxport-get-deviceid-vb">IFaxPort::get_DeviceId</a> property to uniquely identify a fax port.

<b>IFaxPort::get_Name</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxport-get-deviceid-vb">IFaxPort::get_DeviceId</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>