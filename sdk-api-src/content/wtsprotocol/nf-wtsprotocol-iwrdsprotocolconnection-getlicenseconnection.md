---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetLicenseConnection
title: IWRdsProtocolConnection::GetLicenseConnection (wtsprotocol.h)
description: Retrieves an IWRdsProtocolLicenseConnection object that is used to begin the client licensing process.
helpviewer_keywords: ["GetLicenseConnection","GetLicenseConnection method [Remote Desktop Services]","GetLicenseConnection method [Remote Desktop Services]","IWRdsProtocolConnection interface","IWRdsProtocolConnection interface [Remote Desktop Services]","GetLicenseConnection method","IWRdsProtocolConnection.GetLicenseConnection","IWRdsProtocolConnection::GetLicenseConnection","termserv.iwrdsprotocolconnection_getlicenseconnection","wtsprotocol/IWRdsProtocolConnection::GetLicenseConnection"]
old-location: termserv\iwrdsprotocolconnection_getlicenseconnection.htm
tech.root: TermServ
ms.assetid: 6c75f80a-0d47-489d-b684-f718326e2b0d
ms.date: 12/05/2018
ms.keywords: GetLicenseConnection, GetLicenseConnection method [Remote Desktop Services], GetLicenseConnection method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetLicenseConnection method, IWRdsProtocolConnection.GetLicenseConnection, IWRdsProtocolConnection::GetLicenseConnection, termserv.iwrdsprotocolconnection_getlicenseconnection, wtsprotocol/IWRdsProtocolConnection::GetLicenseConnection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWRdsProtocolConnection::GetLicenseConnection
 - wtsprotocol/IWRdsProtocolConnection::GetLicenseConnection
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
 - IWRdsProtocolConnection.GetLicenseConnection
---

# IWRdsProtocolConnection::GetLicenseConnection


## -description

Retrieves an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection">IWRdsProtocolLicenseConnection</a> object that is used to begin the client licensing process. The protocol must add a reference to this object before returning. When the Remote Desktop Services service has finished the licensing process, it will release the reference.

## -parameters

### -param ppLicenseConnection [out]

The address of a pointer to an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection">IWRdsProtocolLicenseConnection</a> interface the receives the license connection object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code. Upon receiving an error, the Remote Desktop Services service will drop the connection.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>