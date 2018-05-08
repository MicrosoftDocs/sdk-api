---
UID: NF:wtsprotocol.IWRdsProtocolLicenseConnection.RequestLicensingCapabilities
title: IWRdsProtocolLicenseConnection::RequestLicensingCapabilities
author: windows-driver-content
description: Requests license capabilities from the client.
old-location: termserv\iwrdsprotocollicenseconnection_requestlicensingcapabilities.htm
old-project: TermServ
ms.assetid: a5814a01-9e4b-4510-b6a5-fa6edc6a15ed
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IWRdsProtocolLicenseConnection interface [Remote Desktop Services],RequestLicensingCapabilities method, IWRdsProtocolLicenseConnection.RequestLicensingCapabilities, IWRdsProtocolLicenseConnection::RequestLicensingCapabilities, RequestLicensingCapabilities, RequestLicensingCapabilities method [Remote Desktop Services], RequestLicensingCapabilities method [Remote Desktop Services],IWRdsProtocolLicenseConnection interface, termserv.iwrdsprotocollicenseconnection_requestlicensingcapabilities, wtsprotocol/IWRdsProtocolLicenseConnection::RequestLicensingCapabilities
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wtsprotocol.h
api_name:
-	IWRdsProtocolLicenseConnection.RequestLicensingCapabilities
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolLicenseConnection::RequestLicensingCapabilities


## -description


Requests license capabilities from the client.


## -parameters




### -param ppLicenseCapabilities [out]

A pointer to a <a href="https://msdn.microsoft.com/975a534e-03f1-4c8f-9de1-42144e31c8cb">WRDS_LICENSE_CAPABILITIES</a> structure that contains information about the client license capabilities.


### -param pcbLicenseCapabilities [in, out]

A pointer to an integer that contains the size of the structure specified by the <i>ppLicensingCapabilities</i> parameter.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/498c31c5-1cb6-41d7-91fb-7409ea03dda0">IWRdsProtocolLicenseConnection</a>
 

 

