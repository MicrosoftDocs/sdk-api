---
UID: NF:wtsprotocol.IWTSProtocolLicenseConnection.RequestClientLicense
title: IWTSProtocolLicenseConnection::RequestClientLicense (wtsprotocol.h)
description: IWTSProtocolLicenseConnection::RequestClientLicense is no longer available. Instead, use IWRdsProtocolLicenseConnection::RequestClientLicense.
helpviewer_keywords: ["IWTSProtocolLicenseConnection interface [Remote Desktop Services]","RequestClientLicense method","IWTSProtocolLicenseConnection.RequestClientLicense","IWTSProtocolLicenseConnection::RequestClientLicense","RequestClientLicense","RequestClientLicense method [Remote Desktop Services]","RequestClientLicense method [Remote Desktop Services]","IWTSProtocolLicenseConnection interface","termserv.iwtsprotocollicenseconnection_requestclientlicense","wtsprotocol/IWTSProtocolLicenseConnection::RequestClientLicense"]
old-location: termserv\iwtsprotocollicenseconnection_requestclientlicense.htm
tech.root: TermServ
ms.assetid: 4740d7a4-aa82-4c9d-b93c-20a974f170ae
ms.date: 12/05/2018
ms.keywords: IWTSProtocolLicenseConnection interface [Remote Desktop Services],RequestClientLicense method, IWTSProtocolLicenseConnection.RequestClientLicense, IWTSProtocolLicenseConnection::RequestClientLicense, RequestClientLicense, RequestClientLicense method [Remote Desktop Services], RequestClientLicense method [Remote Desktop Services],IWTSProtocolLicenseConnection interface, termserv.iwtsprotocollicenseconnection_requestclientlicense, wtsprotocol/IWTSProtocolLicenseConnection::RequestClientLicense
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWTSProtocolLicenseConnection::RequestClientLicense
 - wtsprotocol/IWTSProtocolLicenseConnection::RequestClientLicense
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolLicenseConnection.RequestClientLicense
---

# IWTSProtocolLicenseConnection::RequestClientLicense


## -description

<p class="CCE_Message">[<b>IWTSProtocolLicenseConnection::RequestClientLicense</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollicenseconnection-requestclientlicense">IWRdsProtocolLicenseConnection::RequestClientLicense</a>.]

Requests a license from the client.

## -parameters

### -param Reserve1 [in]

A pointer to a byte array that contains additional data that can be acted upon by the client.

### -param Reserve2 [in]

An integer that contains the size, in bytes, of the data specified by the <i>Reserve1</i> parameter.

### -param ppClientLicense [out]

A pointer to a byte array that contains the license request.

### -param pcbClientLicense [in, out]

An integer that contains the size, in bytes, of the request specified by the <i>ppClientLicense</i> parameter.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

For more information about the byte arrays exchanged in this call, see <a href="/openspecs/windows_protocols/ms-rdpele/3d3f160a-3ab3-4dfb-ba4e-47c27cd79409">[MS-RDPELE]: Remote Desktop Protocol: Licensing Extension</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollicenseconnection">IWTSProtocolLicenseConnection</a>