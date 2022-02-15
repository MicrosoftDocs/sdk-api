---
UID: NF:faxcomex.IFaxServer.RegisterInboundRoutingExtension
title: IFaxServer::RegisterInboundRoutingExtension (faxcomex.h)
description: The IFaxServer::RegisterInboundRoutingExtension method registers a fax inbound routing extension with the fax service. Registration takes place after the fax service restarts.
helpviewer_keywords: ["IFaxServer interface [Fax Service]","RegisterInboundRoutingExtension method","IFaxServer.RegisterInboundRoutingExtension","IFaxServer::RegisterInboundRoutingExtension","RegisterInboundRoutingExtension","RegisterInboundRoutingExtension method [Fax Service]","RegisterInboundRoutingExtension method [Fax Service]","IFaxServer interface","_mfax_faxserver.registerinboundroutingextension","fax._mfax_faxserver_cpp_mfax_faxserver_registerinboundroutingextension_cpp","fax._mfax_faxserver_registerinboundroutingextension","faxcomex/IFaxServer::RegisterInboundRoutingExtension"]
old-location: fax\_mfax_faxserver_cpp_mfax_faxserver_registerinboundroutingextension_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_9kfi.htm
ms.date: 12/05/2018
ms.keywords: IFaxServer interface [Fax Service],RegisterInboundRoutingExtension method, IFaxServer.RegisterInboundRoutingExtension, IFaxServer::RegisterInboundRoutingExtension, RegisterInboundRoutingExtension, RegisterInboundRoutingExtension method [Fax Service], RegisterInboundRoutingExtension method [Fax Service],IFaxServer interface, _mfax_faxserver.registerinboundroutingextension, fax._mfax_faxserver_cpp_mfax_faxserver_registerinboundroutingextension_cpp, fax._mfax_faxserver_registerinboundroutingextension, faxcomex/IFaxServer::RegisterInboundRoutingExtension
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
 - IFaxServer::RegisterInboundRoutingExtension
 - faxcomex/IFaxServer::RegisterInboundRoutingExtension
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
 - IFaxServer.RegisterInboundRoutingExtension
 - IFaxServer.RegisterInboundRoutingExtension
---

# IFaxServer::RegisterInboundRoutingExtension


## -description

The <b>IFaxServer::RegisterInboundRoutingExtension</b> method registers a fax inbound routing extension with the fax service. Registration takes place after the fax service restarts.

## -parameters

### -param bstrExtensionName

Type: <b>BSTR</b>

String that specifies the internal name of the fax routing extension DLL.

### -param bstrFriendlyName

Type: <b>BSTR</b>

String to associate with the fax routing extension DLL. This is the routing extension's user-friendly name, suitable for display.

### -param bstrImageName

Type: <b>BSTR</b>

String that specifies the full path and file name for the fax routing extension DLL. The path can include valid environment variables, for example, %SYSTEMDRIVE% and %SYSTEMROOT%.

### -param vMethods

Type: <b>VARIANT</b>


<a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> that specifies a safearray of <b>BSTR</b>s. The array must be unidimensional, it cannot be empty, and it must have a lower limit of zero. Each item (string) in the array must identify a routing method. The string must have the following format: Method name; Friendly name; Function Name; Method GUID

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Only an administrator can register a routing extension. Also, this method works only on the local fax server.

This property is not supported in Windows XP, and will return the error: <a href="/previous-versions/windows/desktop/fax/-mfax-fax-error-codes">FAX_E_NOT_SUPPORTED_ON_THIS_SKU</a>. 

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver">IFaxServer</a>