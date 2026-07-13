---
UID: NF:faxcomex.IFaxServer.RegisterDeviceProvider
title: IFaxServer::RegisterDeviceProvider (faxcomex.h)
description: The IFaxServer::RegisterDeviceProvider method registers a fax service provider (FSP) with the fax service. Registration takes place after the fax service restarts.
helpviewer_keywords: ["IFaxServer interface [Fax Service]","RegisterDeviceProvider method","IFaxServer.RegisterDeviceProvider","IFaxServer::RegisterDeviceProvider","RegisterDeviceProvider","RegisterDeviceProvider method [Fax Service]","RegisterDeviceProvider method [Fax Service]","IFaxServer interface","_mfax_faxserver.registerdeviceprovider","fax._mfax_faxserver_cpp_mfax_faxserver_registerdeviceprovider_cpp","fax._mfax_faxserver_registerdeviceprovider","faxcomex/IFaxServer::RegisterDeviceProvider"]
old-location: fax\_mfax_faxserver_cpp_mfax_faxserver_registerdeviceprovider_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_59ki.htm
ms.date: 12/05/2018
ms.keywords: IFaxServer interface [Fax Service],RegisterDeviceProvider method, IFaxServer.RegisterDeviceProvider, IFaxServer::RegisterDeviceProvider, RegisterDeviceProvider, RegisterDeviceProvider method [Fax Service], RegisterDeviceProvider method [Fax Service],IFaxServer interface, _mfax_faxserver.registerdeviceprovider, fax._mfax_faxserver_cpp_mfax_faxserver_registerdeviceprovider_cpp, fax._mfax_faxserver_registerdeviceprovider, faxcomex/IFaxServer::RegisterDeviceProvider
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
 - IFaxServer::RegisterDeviceProvider
 - faxcomex/IFaxServer::RegisterDeviceProvider
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
 - IFaxServer.RegisterDeviceProvider
---

## -description

The <b>IFaxServer::RegisterDeviceProvider</b> method registers a fax service provider (FSP) with the fax service. Registration takes place after the fax service restarts.

## -parameters

### -param bstrGUID

Type: <b>BSTR</b>

Null-terminated string that contains the GUID that uniquely identifies the FSP that is registering.

### -param bstrFriendlyName

Type: <b>BSTR</b>

Null-terminated string that contains the user-friendly name to display for the FSP that is registering.

### -param bstrImageName

Type: <b>BSTR</b>

Null-terminated string that contains the fully qualified path and file name of the FSPÂ DLL.

### -param TspName

Type: <b>BSTR</b>

Null-terminated string that contains the name of the telephony service provider associated with the devices for the FSP.

### -param lFSPIVersion

Type: <b>long</b>

A <b>long</b> value that indicates the version of the FSP. Should be equal to 0x00010000.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Only an administrator can register a FSP.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver">IFaxServer</a>