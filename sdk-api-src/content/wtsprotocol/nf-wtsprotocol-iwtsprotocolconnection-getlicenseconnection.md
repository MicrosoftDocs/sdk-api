---
UID: NF:wtsprotocol.IWTSProtocolConnection.GetLicenseConnection
title: IWTSProtocolConnection::GetLicenseConnection (wtsprotocol.h)
description: IWTSProtocolConnection::GetLicenseConnection is no longer available. Instead, use IWRdsProtocolConnection::GetLicenseConnection.
helpviewer_keywords: ["GetLicenseConnection","GetLicenseConnection method [Remote Desktop Services]","GetLicenseConnection method [Remote Desktop Services]","IWTSProtocolConnection interface","IWTSProtocolConnection interface [Remote Desktop Services]","GetLicenseConnection method","IWTSProtocolConnection.GetLicenseConnection","IWTSProtocolConnection::GetLicenseConnection","termserv.iwtsprotocolconnection_getlicenseconnection","wtsprotocol/IWTSProtocolConnection::GetLicenseConnection"]
old-location: termserv\iwtsprotocolconnection_getlicenseconnection.htm
tech.root: TermServ
ms.assetid: 714e2479-54b2-4899-9fbd-68fa35051f58
ms.date: 12/05/2018
ms.keywords: GetLicenseConnection, GetLicenseConnection method [Remote Desktop Services], GetLicenseConnection method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],GetLicenseConnection method, IWTSProtocolConnection.GetLicenseConnection, IWTSProtocolConnection::GetLicenseConnection, termserv.iwtsprotocolconnection_getlicenseconnection, wtsprotocol/IWTSProtocolConnection::GetLicenseConnection
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
 - IWTSProtocolConnection::GetLicenseConnection
 - wtsprotocol/IWTSProtocolConnection::GetLicenseConnection
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
 - IWTSProtocolConnection.GetLicenseConnection
---

# IWTSProtocolConnection::GetLicenseConnection


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection::GetLicenseConnection</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getlicenseconnection">IWRdsProtocolConnection::GetLicenseConnection</a>.]

Retrieves an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollicenseconnection">IWTSProtocolLicenseConnection</a> object that is used to begin the client licensing process. The protocol must add a reference to this object before returning. When the Remote Desktop Services service has finished the licensing process, it will release the reference.

## -parameters

### -param ppLicenseConnection [out]

The address of a pointer to an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollicenseconnection">IWTSProtocolLicenseConnection</a> interface.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>