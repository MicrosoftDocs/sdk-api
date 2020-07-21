---
UID: NF:wtsprotocol.IWRdsProtocolLicenseConnection.SendClientLicense
title: IWRdsProtocolLicenseConnection::SendClientLicense (wtsprotocol.h)
description: Sends a license to the client.
helpviewer_keywords: ["IWRdsProtocolLicenseConnection interface [Remote Desktop Services]","SendClientLicense method","IWRdsProtocolLicenseConnection.SendClientLicense","IWRdsProtocolLicenseConnection::SendClientLicense","SendClientLicense","SendClientLicense method [Remote Desktop Services]","SendClientLicense method [Remote Desktop Services]","IWRdsProtocolLicenseConnection interface","termserv.iwrdsprotocollicenseconnection_sendclientlicense","wtsprotocol/IWRdsProtocolLicenseConnection::SendClientLicense"]
old-location: termserv\iwrdsprotocollicenseconnection_sendclientlicense.htm
tech.root: TermServ
ms.assetid: a758f6c8-1f84-4c20-857c-019cde68915c
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolLicenseConnection interface [Remote Desktop Services],SendClientLicense method, IWRdsProtocolLicenseConnection.SendClientLicense, IWRdsProtocolLicenseConnection::SendClientLicense, SendClientLicense, SendClientLicense method [Remote Desktop Services], SendClientLicense method [Remote Desktop Services],IWRdsProtocolLicenseConnection interface, termserv.iwrdsprotocollicenseconnection_sendclientlicense, wtsprotocol/IWRdsProtocolLicenseConnection::SendClientLicense
f1_keywords:
- wtsprotocol/IWRdsProtocolLicenseConnection.SendClientLicense
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>. The remote connection manager logs any errors that you return. 




## -remarks



For more information about the byte arrays exchanged in this call (such as the <b>SERVER_NEW_LICENSE</b>, <b>SERVER_PLATFORM_CHALLENGE</b>, <b>SERVER_LICENSE_REQUEST</b>, and <b>SERVER_UPGRADE_LICENSE</b> packet structures), see <a href="https://msdn.microsoft.com/library/cc241880(PROT.10).aspx">[MS-RDPELE]: Remote Desktop Protocol: Licensing Extension</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection">IWRdsProtocolLicenseConnection</a>
 

 

