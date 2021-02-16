---
UID: NF:wtsprotocol.IWTSProtocolLicenseConnection.ProtocolComplete
title: IWTSProtocolLicenseConnection::ProtocolComplete (wtsprotocol.h)
description: IWTSProtocolLicenseConnection::ProtocolComplete is no longer available. Instead, use IWRdsProtocolLicenseConnection::ProtocolComplete.
helpviewer_keywords: ["IWTSProtocolLicenseConnection interface [Remote Desktop Services]","ProtocolComplete method","IWTSProtocolLicenseConnection.ProtocolComplete","IWTSProtocolLicenseConnection::ProtocolComplete","ProtocolComplete","ProtocolComplete method [Remote Desktop Services]","ProtocolComplete method [Remote Desktop Services]","IWTSProtocolLicenseConnection interface","termserv.iwtsprotocollicenseconnection_protocolcomplete","wtsprotocol/IWTSProtocolLicenseConnection::ProtocolComplete"]
old-location: termserv\iwtsprotocollicenseconnection_protocolcomplete.htm
tech.root: TermServ
ms.assetid: 3a615e25-51d0-49eb-ae0f-185fd3a0ea23
ms.date: 12/05/2018
ms.keywords: IWTSProtocolLicenseConnection interface [Remote Desktop Services],ProtocolComplete method, IWTSProtocolLicenseConnection.ProtocolComplete, IWTSProtocolLicenseConnection::ProtocolComplete, ProtocolComplete, ProtocolComplete method [Remote Desktop Services], ProtocolComplete method [Remote Desktop Services],IWTSProtocolLicenseConnection interface, termserv.iwtsprotocollicenseconnection_protocolcomplete, wtsprotocol/IWTSProtocolLicenseConnection::ProtocolComplete
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
 - IWTSProtocolLicenseConnection::ProtocolComplete
 - wtsprotocol/IWTSProtocolLicenseConnection::ProtocolComplete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolLicenseConnection.ProtocolComplete
---

# IWTSProtocolLicenseConnection::ProtocolComplete


## -description

<p class="CCE_Message">[<b>IWTSProtocolLicenseConnection::ProtocolComplete</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollicenseconnection-protocolcomplete">IWRdsProtocolLicenseConnection::ProtocolComplete</a>.]

Notifies the protocol whether the licensing process completed successfully.

## -parameters

### -param ulComplete [in]

An integer that specifies whether the licensing process ended successfully. A value of one (1) means success. All other values indicate failure.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollicenseconnection">IWTSProtocolLicenseConnection</a>