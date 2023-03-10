---
UID: NF:wtsprotocol.IWRdsProtocolListener.GetSettings
title: IWRdsProtocolListener::GetSettings (wtsprotocol.h)
description: Gets the listener setting information for client connection requests.
helpviewer_keywords: ["GetSettings","GetSettings method [Remote Desktop Services]","GetSettings method [Remote Desktop Services]","IWRdsProtocolListener interface","IWRdsProtocolListener interface [Remote Desktop Services]","GetSettings method","IWRdsProtocolListener.GetSettings","IWRdsProtocolListener::GetSettings","termserv.iwrdsprotocollistener_getsettings","wtsprotocol/IWRdsProtocolListener::GetSettings"]
old-location: termserv\iwrdsprotocollistener_getsettings.htm
tech.root: TermServ
ms.assetid: 644eaa8f-776d-49de-af23-de9faef80e74
ms.date: 12/05/2018
ms.keywords: GetSettings, GetSettings method [Remote Desktop Services], GetSettings method [Remote Desktop Services],IWRdsProtocolListener interface, IWRdsProtocolListener interface [Remote Desktop Services],GetSettings method, IWRdsProtocolListener.GetSettings, IWRdsProtocolListener::GetSettings, termserv.iwrdsprotocollistener_getsettings, wtsprotocol/IWRdsProtocolListener::GetSettings
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
 - IWRdsProtocolListener::GetSettings
 - wtsprotocol/IWRdsProtocolListener::GetSettings
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
 - IWRdsProtocolListener.GetSettings
---

# IWRdsProtocolListener::GetSettings


## -description

Gets the listener setting information for client connection requests.

## -parameters

### -param WRdsListenerSettingLevel [in]

The listener setting level to use.

### -param pWRdsListenerSettings [out]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_listener_settings">WRDS_LISTENER_SETTINGS</a> structure that contains the returned listener settings.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, 
return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, 
see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener">IWRdsProtocolListener</a>