---
UID: NF:wtsprotocol.IWTSProtocolLicenseConnection.RequestClientLicense
title: IWTSProtocolLicenseConnection::RequestClientLicense
author: windows-sdk-content
description: IWTSProtocolLicenseConnection::RequestClientLicense is no longer available. Instead, use IWRdsProtocolLicenseConnection::RequestClientLicense.
old-location: termserv\iwtsprotocollicenseconnection_requestclientlicense.htm
tech.root: termserv
ms.assetid: 4740d7a4-aa82-4c9d-b93c-20a974f170ae
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWTSProtocolLicenseConnection interface [Remote Desktop Services],RequestClientLicense method, IWTSProtocolLicenseConnection.RequestClientLicense, IWTSProtocolLicenseConnection::RequestClientLicense, RequestClientLicense, RequestClientLicense method [Remote Desktop Services], RequestClientLicense method [Remote Desktop Services],IWTSProtocolLicenseConnection interface, termserv.iwtsprotocollicenseconnection_requestclientlicense, wtsprotocol/IWTSProtocolLicenseConnection::RequestClientLicense
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
 - IWTSProtocolLicenseConnection.RequestClientLicense
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSProtocolLicenseConnection::RequestClientLicense


## -description


<p class="CCE_Message">[<b>IWTSProtocolLicenseConnection::RequestClientLicense</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/73660029-2d2e-4240-babe-208daa164290">IWRdsProtocolLicenseConnection::RequestClientLicense</a>.]

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



For more information about the byte arrays exchanged in this call, see <a href="http://go.microsoft.com/fwlink/p/?linkid=157338">[MS-RDPELE]: Remote Desktop Protocol: Licensing Extension</a>.




## -see-also




<a href="https://msdn.microsoft.com/3f6925b6-c712-40c6-8b48-7df8ef4a9872">IWTSProtocolLicenseConnection</a>
 

 

