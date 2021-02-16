---
UID: NF:wtsprotocol.IWRdsProtocolLicenseConnection.RequestClientLicense
title: IWRdsProtocolLicenseConnection::RequestClientLicense (wtsprotocol.h)
description: Requests a license from the client.
helpviewer_keywords: ["IWRdsProtocolLicenseConnection interface [Remote Desktop Services]","RequestClientLicense method","IWRdsProtocolLicenseConnection.RequestClientLicense","IWRdsProtocolLicenseConnection::RequestClientLicense","RequestClientLicense","RequestClientLicense method [Remote Desktop Services]","RequestClientLicense method [Remote Desktop Services]","IWRdsProtocolLicenseConnection interface","termserv.iwrdsprotocollicenseconnection_requestclientlicense","wtsprotocol/IWRdsProtocolLicenseConnection::RequestClientLicense"]
old-location: termserv\iwrdsprotocollicenseconnection_requestclientlicense.htm
tech.root: TermServ
ms.assetid: 73660029-2d2e-4240-babe-208daa164290
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolLicenseConnection interface [Remote Desktop Services],RequestClientLicense method, IWRdsProtocolLicenseConnection.RequestClientLicense, IWRdsProtocolLicenseConnection::RequestClientLicense, RequestClientLicense, RequestClientLicense method [Remote Desktop Services], RequestClientLicense method [Remote Desktop Services],IWRdsProtocolLicenseConnection interface, termserv.iwrdsprotocollicenseconnection_requestclientlicense, wtsprotocol/IWRdsProtocolLicenseConnection::RequestClientLicense
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - IWRdsProtocolLicenseConnection::RequestClientLicense
 - wtsprotocol/IWRdsProtocolLicenseConnection::RequestClientLicense
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolLicenseConnection.RequestClientLicense
---

# IWRdsProtocolLicenseConnection::RequestClientLicense


## -description

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

For more information about the byte arrays exchanged in this call (such as the <b>CLIENT_LICENSE_INFO</b>, <b>CLIENT_NEW_LICENSE_REQUEST</b>, and <b>CLIENT_PLATFORM_CHALLENGE_RESPONSE</b> packet structures), see <a href="/openspecs/windows_protocols/ms-rdpele/3d3f160a-3ab3-4dfb-ba4e-47c27cd79409">[MS-RDPELE]: Remote Desktop Protocol: Licensing Extension</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection">IWRdsProtocolLicenseConnection</a>