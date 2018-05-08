---
UID: NF:wtsprotocol.IWTSProtocolLicenseConnection.SendClientLicense
title: IWTSProtocolLicenseConnection::SendClientLicense
author: windows-driver-content
description: IWTSProtocolLicenseConnection::SendClientLicense is no longer available. Instead, use IWRdsProtocolLicenseConnection::SendClientLicense.
old-location: termserv\iwtsprotocollicenseconnection_sendclientlicense.htm
old-project: TermServ
ms.assetid: cafd23ed-2085-4d58-a9b1-1918995fa09c
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IWTSProtocolLicenseConnection interface [Remote Desktop Services],SendClientLicense method, IWTSProtocolLicenseConnection.SendClientLicense, IWTSProtocolLicenseConnection::SendClientLicense, SendClientLicense, SendClientLicense method [Remote Desktop Services], SendClientLicense method [Remote Desktop Services],IWTSProtocolLicenseConnection interface, termserv.iwtsprotocollicenseconnection_sendclientlicense, wtsprotocol/IWTSProtocolLicenseConnection::SendClientLicense
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
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wtsprotocol.h
api_name:
-	IWTSProtocolLicenseConnection.SendClientLicense
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolLicenseConnection::SendClientLicense


## -description


<p class="CCE_Message">[<b>IWTSProtocolLicenseConnection::SendClientLicense</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/a758f6c8-1f84-4c20-857c-019cde68915c">IWRdsProtocolLicenseConnection::SendClientLicense</a>.]

Sends a license to the client.


## -parameters




### -param pClientLicense [in]

A pointer to a byte array that contains the license.


### -param cbClientLicense [in]

An integer that contains the size, in bytes, of the license.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. The remote connection manager logs any errors that you return. 




## -remarks



For more information about the byte arrays exchanged in this call, see <a href="http://go.microsoft.com/fwlink/p/?linkid=157338">[MS-RDPELE]: Remote Desktop Protocol: Licensing Extension</a>.




## -see-also




<a href="https://msdn.microsoft.com/3f6925b6-c712-40c6-8b48-7df8ef4a9872">IWTSProtocolLicenseConnection</a>
 

 

