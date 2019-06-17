---
UID: NF:wtsprotocol.IWTSProtocolConnection.GetUserData
title: IWTSProtocolConnection::GetUserData (wtsprotocol.h)
author: windows-sdk-content
description: IWTSProtocolConnection::GetUserData is no longer available. Instead, use IWRdsProtocolSettings::MergeSettings.
old-location: termserv\iwtsprotocolconnection_getuserdata.htm
tech.root: TermServ
ms.assetid: fa77c537-c78d-4fe3-b597-787efd740cf6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetUserData, GetUserData method [Remote Desktop Services], GetUserData method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],GetUserData method, IWTSProtocolConnection.GetUserData, IWTSProtocolConnection::GetUserData, termserv.iwtsprotocolconnection_getuserdata, wtsprotocol/IWTSProtocolConnection::GetUserData
ms.topic: method
f1_keywords: ["wtsprotocol/IWTSProtocolConnection.GetUserData"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolConnection.GetUserData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSProtocolConnection::GetUserData


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::GetUserData</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolsettings-mergesettings">IWRdsProtocolSettings::MergeSettings</a>.]

Sends merged policy settings to the protocol and requests user policy settings from the protocol.


## -parameters




### -param pPolicyData [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wtsdefs/ns-wtsdefs-_wts_policy_data">WTS_POLICY_DATA</a> structure that contains the merged Group Policy values.


### -param pClientData [in, out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wtsdefs/ns-wtsdefs-_wts_user_data">WTS_USER_DATA</a> structure that contains client property information.


## -remarks



The Remote Desktop Services service merges all policy data, including listener settings, client-provided data, and Group Policy data, before calling this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>
 

 

