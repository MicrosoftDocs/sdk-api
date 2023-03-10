---
UID: NF:wtsprotocol.IWTSProtocolLicenseConnection.RequestLicensingCapabilities
title: IWTSProtocolLicenseConnection::RequestLicensingCapabilities (wtsprotocol.h)
description: IWTSProtocolLicenseConnection::RequestLicensingCapabilities is no longer available. Instead, use IWRdsProtocolLicenseConnection::RequestLicensingCapabilities.
helpviewer_keywords: ["IWTSProtocolLicenseConnection interface [Remote Desktop Services]","RequestLicensingCapabilities method","IWTSProtocolLicenseConnection.RequestLicensingCapabilities","IWTSProtocolLicenseConnection::RequestLicensingCapabilities","RequestLicensingCapabilities","RequestLicensingCapabilities method [Remote Desktop Services]","RequestLicensingCapabilities method [Remote Desktop Services]","IWTSProtocolLicenseConnection interface","termserv.iwtsprotocollicenseconnection_requestlicensingcapabilities","wtsprotocol/IWTSProtocolLicenseConnection::RequestLicensingCapabilities"]
old-location: termserv\iwtsprotocollicenseconnection_requestlicensingcapabilities.htm
tech.root: TermServ
ms.assetid: ff6123f6-4d78-41d1-8093-916f01de09ef
ms.date: 12/05/2018
ms.keywords: IWTSProtocolLicenseConnection interface [Remote Desktop Services],RequestLicensingCapabilities method, IWTSProtocolLicenseConnection.RequestLicensingCapabilities, IWTSProtocolLicenseConnection::RequestLicensingCapabilities, RequestLicensingCapabilities, RequestLicensingCapabilities method [Remote Desktop Services], RequestLicensingCapabilities method [Remote Desktop Services],IWTSProtocolLicenseConnection interface, termserv.iwtsprotocollicenseconnection_requestlicensingcapabilities, wtsprotocol/IWTSProtocolLicenseConnection::RequestLicensingCapabilities
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
 - IWTSProtocolLicenseConnection::RequestLicensingCapabilities
 - wtsprotocol/IWTSProtocolLicenseConnection::RequestLicensingCapabilities
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
 - IWTSProtocolLicenseConnection.RequestLicensingCapabilities
---

# IWTSProtocolLicenseConnection::RequestLicensingCapabilities


## -description

<p class="CCE_Message">[<b>IWTSProtocolLicenseConnection::RequestLicensingCapabilities</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollicenseconnection-requestlicensingcapabilities">IWRdsProtocolLicenseConnection::RequestLicensingCapabilities</a>.]

Requests license capabilities from the client.

## -parameters

### -param ppLicenseCapabilities [out]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_license_capabilities">WTS_LICENSE_CAPABILITIES</a> structure that contains information about the client license capabilities.

### -param pcbLicenseCapabilities [in, out]

A pointer to an integer that contains the size of the structure specified by the <i>ppLicensingCapabilities</i> parameter.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollicenseconnection">IWTSProtocolLicenseConnection</a>