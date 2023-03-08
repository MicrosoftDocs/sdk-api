---
UID: NF:faxcomex.IFaxServer.GetDevices
title: IFaxServer::GetDevices (faxcomex.h)
description: The IFaxServer::GetDevices method creates a IFaxDevices interface, a collection of all the fax devices exposed by all the fax service providers (FSPs) currently registered with the fax service.
helpviewer_keywords: ["GetDevices","GetDevices method [Fax Service]","GetDevices method [Fax Service]","IFaxServer interface","IFaxServer interface [Fax Service]","GetDevices method","IFaxServer.GetDevices","IFaxServer::GetDevices","_mfax_faxserver.getdevices_cpp","fax._mfax_faxserver_getdevices_cpp","faxcomex/IFaxServer::GetDevices"]
old-location: fax\_mfax_faxserver_getdevices_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7hrn_cpp.htm
ms.date: 12/05/2018
ms.keywords: GetDevices, GetDevices method [Fax Service], GetDevices method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],GetDevices method, IFaxServer.GetDevices, IFaxServer::GetDevices, _mfax_faxserver.getdevices_cpp, fax._mfax_faxserver_getdevices_cpp, faxcomex/IFaxServer::GetDevices
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
 - IFaxServer::GetDevices
 - faxcomex/IFaxServer::GetDevices
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
 - IFaxServer.GetDevices
---

# IFaxServer::GetDevices


## -description

The <b>IFaxServer::GetDevices</b> method creates a <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdevices">IFaxDevices</a> interface, a collection of all the fax devices exposed by all the fax service providers (FSPs) currently registered with the fax service.

## -parameters

### -param ppFaxDevices [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdevices">IFaxDevices</a>**</b>

An address of a pointer that receives a <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdevices">IFaxDevices</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can use the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdevices">IFaxDevices</a> interface to enumerate the fax devices associated with a connected fax server and to create <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdevice">IFaxDevice</a> interfaces for them.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver">IFaxServer</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-configuring-a-fax-device">Visual Basic Example</a>