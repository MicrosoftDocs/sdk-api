---
UID: NF:wtsprotocol.IWRdsProtocolLicenseConnection.SendClientLicense
title: IWRdsProtocolLicenseConnection::SendClientLicense
author: windows-sdk-content
description: Sends a license to the client.
old-location: termserv\iwrdsprotocollicenseconnection_sendclientlicense.htm
tech.root: termserv
ms.assetid: a758f6c8-1f84-4c20-857c-019cde68915c
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IWRdsProtocolLicenseConnection interface [Remote Desktop Services],SendClientLicense method, IWRdsProtocolLicenseConnection.SendClientLicense, IWRdsProtocolLicenseConnection::SendClientLicense, SendClientLicense, SendClientLicense method [Remote Desktop Services], SendClientLicense method [Remote Desktop Services],IWRdsProtocolLicenseConnection interface, termserv.iwrdsprotocollicenseconnection_sendclientlicense, wtsprotocol/IWRdsProtocolLicenseConnection::SendClientLicense
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
 - IWRdsProtocolLicenseConnection.SendClientLicense
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolLicenseConnection::SendClientLicense


## -description


Sends a license to the client.


## -parameters




### -param pClientLicense [in]

A pointer to a byte array that contains the license.


### -param cbClientLicense [in]

An integer that contains the size, in bytes, of the license.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. The remote connection manager logs any errors that you return. 




## -remarks



For more information about the byte arrays exchanged in this call (such as the <b>SERVER_NEW_LICENSE</b>, <b>SERVER_PLATFORM_CHALLENGE</b>, <b>SERVER_LICENSE_REQUEST</b>, and <b>SERVER_UPGRADE_LICENSE</b> packet structures), see <a href="http://go.microsoft.com/fwlink/p/?linkid=157338">[MS-RDPELE]: Remote Desktop Protocol: Licensing Extension</a>.




## -see-also




<a href="https://msdn.microsoft.com/498c31c5-1cb6-41d7-91fb-7409ea03dda0">IWRdsProtocolLicenseConnection</a>
 

 

