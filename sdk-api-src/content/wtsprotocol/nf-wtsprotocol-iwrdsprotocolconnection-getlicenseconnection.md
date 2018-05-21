---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetLicenseConnection
title: IWRdsProtocolConnection::GetLicenseConnection
author: windows-driver-content
description: Retrieves an IWRdsProtocolLicenseConnection object that is used to begin the client licensing process.
old-location: termserv\iwrdsprotocolconnection_getlicenseconnection.htm
old-project: TermServ
ms.assetid: 6c75f80a-0d47-489d-b684-f718326e2b0d
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: GetLicenseConnection, GetLicenseConnection method [Remote Desktop Services], GetLicenseConnection method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetLicenseConnection method, IWRdsProtocolConnection.GetLicenseConnection, IWRdsProtocolConnection::GetLicenseConnection, termserv.iwrdsprotocolconnection_getlicenseconnection, wtsprotocol/IWRdsProtocolConnection::GetLicenseConnection
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
-	IWRdsProtocolConnection.GetLicenseConnection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolConnection::GetLicenseConnection


## -description


Retrieves an <a href="https://msdn.microsoft.com/498c31c5-1cb6-41d7-91fb-7409ea03dda0">IWRdsProtocolLicenseConnection</a> object that is used to begin the client licensing process. The protocol must add a reference to this object before returning. When the Remote Desktop Services service has finished the licensing process, it will release the reference.


## -parameters




### -param ppLicenseConnection [out]

The address of a pointer to an <a href="https://msdn.microsoft.com/498c31c5-1cb6-41d7-91fb-7409ea03dda0">IWRdsProtocolLicenseConnection</a> interface the receives the license connection object.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code. Upon receiving an error, the Remote Desktop Services service will drop the connection.




## -see-also




<a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a>
 

 

