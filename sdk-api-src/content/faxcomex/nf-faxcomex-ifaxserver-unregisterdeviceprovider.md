---
UID: NF:faxcomex.IFaxServer.UnregisterDeviceProvider
title: IFaxServer::UnregisterDeviceProvider (faxcomex.h)
description: The IFaxServer::UnregisterDeviceProvider method unregisters (removes the registration of) an existing device provider. Unregistration will take place only after the fax server is restarted.
helpviewer_keywords: ["IFaxServer interface [Fax Service]","UnregisterDeviceProvider method","IFaxServer.UnregisterDeviceProvider","IFaxServer::UnregisterDeviceProvider","UnregisterDeviceProvider","UnregisterDeviceProvider method [Fax Service]","UnregisterDeviceProvider method [Fax Service]","IFaxServer interface","_mfax_faxserver.unregisterdeviceprovider","fax._mfax_faxserver_cpp_mfax_faxserver_unregisterdeviceprovider_cpp","fax._mfax_faxserver_unregisterdeviceprovider","faxcomex/IFaxServer::UnregisterDeviceProvider"]
old-location: fax\_mfax_faxserver_cpp_mfax_faxserver_unregisterdeviceprovider_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8h82.htm
ms.date: 12/05/2018
ms.keywords: IFaxServer interface [Fax Service],UnregisterDeviceProvider method, IFaxServer.UnregisterDeviceProvider, IFaxServer::UnregisterDeviceProvider, UnregisterDeviceProvider, UnregisterDeviceProvider method [Fax Service], UnregisterDeviceProvider method [Fax Service],IFaxServer interface, _mfax_faxserver.unregisterdeviceprovider, fax._mfax_faxserver_cpp_mfax_faxserver_unregisterdeviceprovider_cpp, fax._mfax_faxserver_unregisterdeviceprovider, faxcomex/IFaxServer::UnregisterDeviceProvider
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
 - IFaxServer::UnregisterDeviceProvider
 - faxcomex/IFaxServer::UnregisterDeviceProvider
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
 - IFaxServer.UnregisterDeviceProvider
 - IFaxServer.UnregisterDeviceProvider
---

# IFaxServer::UnregisterDeviceProvider


## -description

The <b>IFaxServer::UnregisterDeviceProvider</b> method unregisters (removes the registration of) an existing device provider. Unregistration will take place only after the fax server is restarted.

## -parameters

### -param bstrUniqueName

Type: <b>BSTR</b>

Required. Specifies the unique name that identifies the FSP that is unregistering.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Only an administrator can unregister a fax service provider.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver">IFaxServer</a>