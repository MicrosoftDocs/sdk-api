---
UID: NF:wtsprotocol.IWRdsProtocolLicenseConnection.RequestLicensingCapabilities
title: IWRdsProtocolLicenseConnection::RequestLicensingCapabilities (wtsprotocol.h)
author: windows-sdk-content
description: Requests license capabilities from the client.
old-location: termserv\iwrdsprotocollicenseconnection_requestlicensingcapabilities.htm
tech.root: TermServ
ms.assetid: a5814a01-9e4b-4510-b6a5-fa6edc6a15ed
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolLicenseConnection interface [Remote Desktop Services],RequestLicensingCapabilities method, IWRdsProtocolLicenseConnection.RequestLicensingCapabilities, IWRdsProtocolLicenseConnection::RequestLicensingCapabilities, RequestLicensingCapabilities, RequestLicensingCapabilities method [Remote Desktop Services], RequestLicensingCapabilities method [Remote Desktop Services],IWRdsProtocolLicenseConnection interface, termserv.iwrdsprotocollicenseconnection_requestlicensingcapabilities, wtsprotocol/IWRdsProtocolLicenseConnection::RequestLicensingCapabilities
ms.topic: method
f1_keywords: 
 - "wtsprotocol/IWRdsProtocolLicenseConnection.RequestLicensingCapabilities"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolLicenseConnection.RequestLicensingCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsProtocolLicenseConnection::RequestLicensingCapabilities


## -description


Requests license capabilities from the client.


## -parameters




### -param ppLicenseCapabilities [out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wtsdefs/ns-wtsdefs-_wts_license_capabilities">WRDS_LICENSE_CAPABILITIES</a> structure that contains information about the client license capabilities.


### -param pcbLicenseCapabilities [in, out]

A pointer to an integer that contains the size of the structure specified by the <i>ppLicensingCapabilities</i> parameter.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection">IWRdsProtocolLicenseConnection</a>
 

 

