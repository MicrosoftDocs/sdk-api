---
UID: NF:faxcomex.IFaxServer.get_APIVersion
title: IFaxServer::get_APIVersion (faxcomex.h)
description: The IFaxServer::get_APIVersion property is a value that indicates the version of the fax server API.
helpviewer_keywords: ["APIVersion property [Fax Service]","APIVersion property [Fax Service]","IFaxServer interface","IFaxServer interface [Fax Service]","APIVersion property","IFaxServer.APIVersion","IFaxServer.get_APIVersion","IFaxServer::APIVersion","IFaxServer::get_APIVersion","_mfax_faxserver.apiversion","fax._mfax_faxserver_apiversion","fax._mfax_faxserver_cpp_mfax_faxserver_apiversion_cpp","faxcomex/IFaxServer::APIVersion","faxcomex/IFaxServer::get_APIVersion","get_APIVersion"]
old-location: fax\_mfax_faxserver_cpp_mfax_faxserver_apiversion_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_43vy.htm
ms.date: 12/05/2018
ms.keywords: APIVersion property [Fax Service], APIVersion property [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],APIVersion property, IFaxServer.APIVersion, IFaxServer.get_APIVersion, IFaxServer::APIVersion, IFaxServer::get_APIVersion, _mfax_faxserver.apiversion, fax._mfax_faxserver_apiversion, fax._mfax_faxserver_cpp_mfax_faxserver_apiversion_cpp, faxcomex/IFaxServer::APIVersion, faxcomex/IFaxServer::get_APIVersion, get_APIVersion
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxServer::get_APIVersion
 - faxcomex/IFaxServer::get_APIVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxServer.APIVersion
 - IFaxServer.get_APIVersion
---

# IFaxServer::get_APIVersion


## -description

The <b>IFaxServer::get_APIVersion</b> property is a value that indicates the version of the fax server API.



This property is read-only.

## -parameters

## -remarks

In general, each new version of the fax server API is fully compatible with previous API versions. When connecting to a fax server using the Component Object Model (COM) objects, the API version of the fax server is not required because the COM layer performs the conversions and mapping to transparently support the fax API version of the server. However, if you want to detect the version of the fax server you are connected to, you can use the <b>IFaxServer::get_APIVersion</b> property.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver">IFaxServer</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-retrieving-server-properties">Visual Basic Example</a>