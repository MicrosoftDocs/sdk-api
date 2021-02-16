---
UID: NF:wtsprotocol.IWTSProtocolLicenseConnection.SendClientLicense
title: IWTSProtocolLicenseConnection::SendClientLicense (wtsprotocol.h)
description: IWTSProtocolLicenseConnection::SendClientLicense is no longer available. Instead, use IWRdsProtocolLicenseConnection::SendClientLicense.
helpviewer_keywords: ["IWTSProtocolLicenseConnection interface [Remote Desktop Services]","SendClientLicense method","IWTSProtocolLicenseConnection.SendClientLicense","IWTSProtocolLicenseConnection::SendClientLicense","SendClientLicense","SendClientLicense method [Remote Desktop Services]","SendClientLicense method [Remote Desktop Services]","IWTSProtocolLicenseConnection interface","termserv.iwtsprotocollicenseconnection_sendclientlicense","wtsprotocol/IWTSProtocolLicenseConnection::SendClientLicense"]
old-location: termserv\iwtsprotocollicenseconnection_sendclientlicense.htm
tech.root: TermServ
ms.assetid: cafd23ed-2085-4d58-a9b1-1918995fa09c
ms.date: 12/05/2018
ms.keywords: IWTSProtocolLicenseConnection interface [Remote Desktop Services],SendClientLicense method, IWTSProtocolLicenseConnection.SendClientLicense, IWTSProtocolLicenseConnection::SendClientLicense, SendClientLicense, SendClientLicense method [Remote Desktop Services], SendClientLicense method [Remote Desktop Services],IWTSProtocolLicenseConnection interface, termserv.iwtsprotocollicenseconnection_sendclientlicense, wtsprotocol/IWTSProtocolLicenseConnection::SendClientLicense
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
 - IWTSProtocolLicenseConnection::SendClientLicense
 - wtsprotocol/IWTSProtocolLicenseConnection::SendClientLicense
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWTSProtocolLicenseConnection.SendClientLicense
---

# IWTSProtocolLicenseConnection::SendClientLicense


## -description

<p class="CCE_Message">[<b>IWTSProtocolLicenseConnection::SendClientLicense</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollicenseconnection-sendclientlicense">IWRdsProtocolLicenseConnection::SendClientLicense</a>.]

Sends a license to the client.

## -parameters

### -param pClientLicense [in]

A pointer to a byte array that contains the license.

### -param cbClientLicense [in]

An integer that contains the size, in bytes, of the license.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>. The remote connection manager logs any errors that you return.

## -remarks

For more information about the byte arrays exchanged in this call, see <a href="/openspecs/windows_protocols/ms-rdpele/3d3f160a-3ab3-4dfb-ba4e-47c27cd79409">[MS-RDPELE]: Remote Desktop Protocol: Licensing Extension</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollicenseconnection">IWTSProtocolLicenseConnection</a>