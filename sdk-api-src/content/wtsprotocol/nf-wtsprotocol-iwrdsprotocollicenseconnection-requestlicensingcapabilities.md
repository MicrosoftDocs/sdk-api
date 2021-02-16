---
UID: NF:wtsprotocol.IWRdsProtocolLicenseConnection.RequestLicensingCapabilities
title: IWRdsProtocolLicenseConnection::RequestLicensingCapabilities (wtsprotocol.h)
description: Requests license capabilities from the client.
helpviewer_keywords: ["IWRdsProtocolLicenseConnection interface [Remote Desktop Services]","RequestLicensingCapabilities method","IWRdsProtocolLicenseConnection.RequestLicensingCapabilities","IWRdsProtocolLicenseConnection::RequestLicensingCapabilities","RequestLicensingCapabilities","RequestLicensingCapabilities method [Remote Desktop Services]","RequestLicensingCapabilities method [Remote Desktop Services]","IWRdsProtocolLicenseConnection interface","termserv.iwrdsprotocollicenseconnection_requestlicensingcapabilities","wtsprotocol/IWRdsProtocolLicenseConnection::RequestLicensingCapabilities"]
old-location: termserv\iwrdsprotocollicenseconnection_requestlicensingcapabilities.htm
tech.root: TermServ
ms.assetid: a5814a01-9e4b-4510-b6a5-fa6edc6a15ed
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolLicenseConnection interface [Remote Desktop Services],RequestLicensingCapabilities method, IWRdsProtocolLicenseConnection.RequestLicensingCapabilities, IWRdsProtocolLicenseConnection::RequestLicensingCapabilities, RequestLicensingCapabilities, RequestLicensingCapabilities method [Remote Desktop Services], RequestLicensingCapabilities method [Remote Desktop Services],IWRdsProtocolLicenseConnection interface, termserv.iwrdsprotocollicenseconnection_requestlicensingcapabilities, wtsprotocol/IWRdsProtocolLicenseConnection::RequestLicensingCapabilities
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
 - IWRdsProtocolLicenseConnection::RequestLicensingCapabilities
 - wtsprotocol/IWRdsProtocolLicenseConnection::RequestLicensingCapabilities
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
 - IWRdsProtocolLicenseConnection.RequestLicensingCapabilities
---

# IWRdsProtocolLicenseConnection::RequestLicensingCapabilities


## -description

Requests license capabilities from the client.

## -parameters

### -param ppLicenseCapabilities [out]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_license_capabilities">WRDS_LICENSE_CAPABILITIES</a> structure that contains information about the client license capabilities.

### -param pcbLicenseCapabilities [in, out]

A pointer to an integer that contains the size of the structure specified by the <i>ppLicensingCapabilities</i> parameter.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection">IWRdsProtocolLicenseConnection</a>