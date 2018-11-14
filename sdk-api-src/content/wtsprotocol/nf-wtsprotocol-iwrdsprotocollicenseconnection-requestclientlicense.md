---
UID: NF:wtsprotocol.IWRdsProtocolLicenseConnection.RequestClientLicense
title: IWRdsProtocolLicenseConnection::RequestClientLicense
author: windows-sdk-content
description: Requests a license from the client.
old-location: termserv\iwrdsprotocollicenseconnection_requestclientlicense.htm
tech.root: termserv
ms.assetid: 73660029-2d2e-4240-babe-208daa164290
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IWRdsProtocolLicenseConnection interface [Remote Desktop Services],RequestClientLicense method, IWRdsProtocolLicenseConnection.RequestClientLicense, IWRdsProtocolLicenseConnection::RequestClientLicense, RequestClientLicense, RequestClientLicense method [Remote Desktop Services], RequestClientLicense method [Remote Desktop Services],IWRdsProtocolLicenseConnection interface, termserv.iwrdsprotocollicenseconnection_requestclientlicense, wtsprotocol/IWRdsProtocolLicenseConnection::RequestClientLicense
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
 - IWRdsProtocolLicenseConnection.RequestClientLicense
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wtsprotocol.h
: 
- IWRdsProtocolLicenseConnection.RequestClientLicense
: 
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



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



For more information about the byte arrays exchanged in this call (such as the <b>CLIENT_LICENSE_INFO</b>, <b>CLIENT_NEW_LICENSE_REQUEST</b>, and <b>CLIENT_PLATFORM_CHALLENGE_RESPONSE</b> packet structures), see <a href="http://go.microsoft.com/fwlink/p/?linkid=157338">[MS-RDPELE]: Remote Desktop Protocol: Licensing Extension</a>.




## -see-also




<a href="https://msdn.microsoft.com/498c31c5-1cb6-41d7-91fb-7409ea03dda0">IWRdsProtocolLicenseConnection</a>
 

 

