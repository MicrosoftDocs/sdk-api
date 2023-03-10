---
UID: NF:faxcom.IFaxServer.get_UseDeviceTsid
title: IFaxServer::get_UseDeviceTsid (faxcom.h)
description: Sets or retrieves the UseDeviceTsid property for a FaxServer object. The UseDeviceTsid property is a Boolean value that indicates whether the fax server uses the device's transmitting station identifier (TSID) instead of a user-specified TSID. (Get)
helpviewer_keywords: ["IFaxServer interface [Fax Service]","UseDeviceTsid property","IFaxServer.UseDeviceTsid","IFaxServer.get_UseDeviceTsid","IFaxServer.put_UseDeviceTsid","IFaxServer::UseDeviceTsid","IFaxServer::get_UseDeviceTsid","IFaxServer::put_UseDeviceTsid","UseDeviceTsid property [Fax Service]","UseDeviceTsid property [Fax Service]","IFaxServer interface","_mfax_ifaxserver_get_usedevicetsid","fax._mfax_ifaxserver_client_mfax_ifaxserver_get_usedevicetsid_cpp","fax._mfax_ifaxserver_get_usedevicetsid","faxcom/IFaxServer::UseDeviceTsid","faxcom/IFaxServer::get_UseDeviceTsid","faxcom/IFaxServer::put_UseDeviceTsid","get_UseDeviceTsid"]
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_usedevicetsid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0xb8.htm
ms.date: 12/05/2018
ms.keywords: IFaxServer interface [Fax Service],UseDeviceTsid property, IFaxServer.UseDeviceTsid, IFaxServer.get_UseDeviceTsid, IFaxServer.put_UseDeviceTsid, IFaxServer::UseDeviceTsid, IFaxServer::get_UseDeviceTsid, IFaxServer::put_UseDeviceTsid, UseDeviceTsid property [Fax Service], UseDeviceTsid property [Fax Service],IFaxServer interface, _mfax_ifaxserver_get_usedevicetsid, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_usedevicetsid_cpp, fax._mfax_ifaxserver_get_usedevicetsid, faxcom/IFaxServer::UseDeviceTsid, faxcom/IFaxServer::get_UseDeviceTsid, faxcom/IFaxServer::put_UseDeviceTsid, get_UseDeviceTsid
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
 - IFaxServer::get_UseDeviceTsid
 - faxcom/IFaxServer::get_UseDeviceTsid
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
 - IFaxServer.UseDeviceTsid
 - IFaxServer.get_UseDeviceTsid
 - IFaxServer.put_UseDeviceTsid
 - IFaxServer.get_UseDeviceTsid
 - IFaxServer.put_UseDeviceTsid
---

# IFaxServer::get_UseDeviceTsid


## -description

Sets or retrieves the <b>UseDeviceTsid</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>UseDeviceTsid</b> property is a Boolean value that indicates whether the fax server uses the device's transmitting station identifier (TSID) instead of a user-specified TSID.

This property is read/write.

## -parameters

## -remarks

To ensure that the TSID for a port is associated with outbound faxes, set the <b>UseDeviceTsid</b> property equal to <b>TRUE</b>. This overrides the TSID a user can optionally specify for an outbound fax by setting the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-tsid-vb">Tsid</a> property.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-tsid-vb">Tsid</a>
