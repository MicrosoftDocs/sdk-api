---
UID: NF:wtsprotocol.IWTSProtocolLicenseConnection.RequestLicensingCapabilities
title: IWTSProtocolLicenseConnection::RequestLicensingCapabilities
author: windows-sdk-content
description: IWTSProtocolLicenseConnection::RequestLicensingCapabilities is no longer available. Instead, use IWRdsProtocolLicenseConnection::RequestLicensingCapabilities.
old-location: termserv\iwtsprotocollicenseconnection_requestlicensingcapabilities.htm
tech.root: termserv
ms.assetid: ff6123f6-4d78-41d1-8093-916f01de09ef
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWTSProtocolLicenseConnection interface [Remote Desktop Services],RequestLicensingCapabilities method, IWTSProtocolLicenseConnection.RequestLicensingCapabilities, IWTSProtocolLicenseConnection::RequestLicensingCapabilities, RequestLicensingCapabilities, RequestLicensingCapabilities method [Remote Desktop Services], RequestLicensingCapabilities method [Remote Desktop Services],IWTSProtocolLicenseConnection interface, termserv.iwtsprotocollicenseconnection_requestlicensingcapabilities, wtsprotocol/IWTSProtocolLicenseConnection::RequestLicensingCapabilities
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolLicenseConnection.RequestLicensingCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSProtocolLicenseConnection::RequestLicensingCapabilities


## -description


<p class="CCE_Message">[<b>IWTSProtocolLicenseConnection::RequestLicensingCapabilities</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/a5814a01-9e4b-4510-b6a5-fa6edc6a15ed">IWRdsProtocolLicenseConnection::RequestLicensingCapabilities</a>.]

Requests license capabilities from the client.


## -parameters




### -param ppLicenseCapabilities [out]

A pointer to a <a href="https://msdn.microsoft.com/975a534e-03f1-4c8f-9de1-42144e31c8cb">WTS_LICENSE_CAPABILITIES</a> structure that contains information about the client license capabilities.


### -param pcbLicenseCapabilities [in, out]

A pointer to an integer that contains the size of the structure specified by the <i>ppLicensingCapabilities</i> parameter.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/3f6925b6-c712-40c6-8b48-7df8ef4a9872">IWTSProtocolLicenseConnection</a>
 

 

