---
UID: NF:wtsprotocol.IWTSProtocolConnection.SendPolicyData
title: IWTSProtocolConnection::SendPolicyData (wtsprotocol.h)
description: IWTSProtocolConnection::SendPolicyData is no longer available. Instead, use IWRdsProtocolManager::NotifySettingsChange.
helpviewer_keywords: ["IWTSProtocolConnection interface [Remote Desktop Services]","SendPolicyData method","IWTSProtocolConnection.SendPolicyData","IWTSProtocolConnection::SendPolicyData","SendPolicyData","SendPolicyData method [Remote Desktop Services]","SendPolicyData method [Remote Desktop Services]","IWTSProtocolConnection interface","termserv.iwtsprotocolconnection_sendpolicydata","wtsprotocol/IWTSProtocolConnection::SendPolicyData"]
old-location: termserv\iwtsprotocolconnection_sendpolicydata.htm
tech.root: TermServ
ms.assetid: b3fcc213-8257-433f-b304-ce19bc209591
ms.date: 12/05/2018
ms.keywords: IWTSProtocolConnection interface [Remote Desktop Services],SendPolicyData method, IWTSProtocolConnection.SendPolicyData, IWTSProtocolConnection::SendPolicyData, SendPolicyData, SendPolicyData method [Remote Desktop Services], SendPolicyData method [Remote Desktop Services],IWTSProtocolConnection interface, termserv.iwtsprotocolconnection_sendpolicydata, wtsprotocol/IWTSProtocolConnection::SendPolicyData
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
 - IWTSProtocolConnection::SendPolicyData
 - wtsprotocol/IWTSProtocolConnection::SendPolicyData
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
 - IWTSProtocolConnection.SendPolicyData
---

# IWTSProtocolConnection::SendPolicyData


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection::SendPolicyData</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-notifysettingschange">IWRdsProtocolManager::NotifySettingsChange</a>.]

Sends computer policy settings to the custom protocol. These settings are a combination of listener policies and Group Policy settings.

## -parameters

### -param pPolicyData [in]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_policy_data">WTS_POLICY_DATA</a> structure that contains computer policy settings.

## -remarks

The <b>SendPolicyData</b> method is the second method called by the Remote Desktop Services service during a connection sequence.  The protocol must call the <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnectioncallback-onready">OnReady</a> method after this method is called, or the connection is dropped.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>