---
UID: NF:faxcomex.IFaxServer.GetDeviceProviders
title: IFaxServer::GetDeviceProviders (faxcomex.h)
description: The IFaxServer::GetDeviceProviders method creates a IFaxDeviceProviders interface, a collection of fax service providers (FSPs) that are currently registered with the fax service.
helpviewer_keywords: ["GetDeviceProviders","GetDeviceProviders method [Fax Service]","GetDeviceProviders method [Fax Service]","IFaxServer interface","IFaxServer interface [Fax Service]","GetDeviceProviders method","IFaxServer.GetDeviceProviders","IFaxServer::GetDeviceProviders","_mfax_faxserver.getdeviceproviders_cpp","fax._mfax_faxserver_getdeviceproviders_cpp","faxcomex/IFaxServer::GetDeviceProviders"]
old-location: fax\_mfax_faxserver_getdeviceproviders_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6xv7_cpp.htm
ms.date: 12/05/2018
ms.keywords: GetDeviceProviders, GetDeviceProviders method [Fax Service], GetDeviceProviders method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],GetDeviceProviders method, IFaxServer.GetDeviceProviders, IFaxServer::GetDeviceProviders, _mfax_faxserver.getdeviceproviders_cpp, fax._mfax_faxserver_getdeviceproviders_cpp, faxcomex/IFaxServer::GetDeviceProviders
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
 - IFaxServer::GetDeviceProviders
 - faxcomex/IFaxServer::GetDeviceProviders
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
 - IFaxServer.GetDeviceProviders
---

# IFaxServer::GetDeviceProviders


## -description

The <b>IFaxServer::GetDeviceProviders</b> method creates a <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceproviders">IFaxDeviceProviders</a> interface, a collection of fax service providers (FSPs) that are currently registered with the fax service. You can use the <b>IFaxDeviceProviders</b> interface to enumerate the FSPs associated with a fax server and to create and access <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceprovider">IFaxDeviceProvider</a> interfaces for them.

## -parameters

### -param ppFaxDeviceProviders [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceproviders">IFaxDeviceProviders</a>**</b>

An address of a pointer that receives a <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceproviders">IFaxDeviceProviders</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver">IFaxServer</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-fax-device-providers">Visual Basic Example</a>