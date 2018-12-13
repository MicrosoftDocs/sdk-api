---
UID: NF:wtsprotocol.IWTSProtocolConnection.GetUserData
title: IWTSProtocolConnection::GetUserData
author: windows-sdk-content
description: IWTSProtocolConnection::GetUserData is no longer available. Instead, use IWRdsProtocolSettings::MergeSettings.
old-location: termserv\iwtsprotocolconnection_getuserdata.htm
tech.root: TermServ
ms.assetid: fa77c537-c78d-4fe3-b597-787efd740cf6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetUserData, GetUserData method [Remote Desktop Services], GetUserData method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],GetUserData method, IWTSProtocolConnection.GetUserData, IWTSProtocolConnection::GetUserData, termserv.iwtsprotocolconnection_getuserdata, wtsprotocol/IWTSProtocolConnection::GetUserData
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
---

# IWTSProtocolConnection::GetUserData


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::GetUserData</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/fa05bcde-e4db-481b-88ab-57d070153517">IWRdsProtocolSettings::MergeSettings</a>.]

Sends merged policy settings to the protocol and requests user policy settings from the protocol.


## -parameters




### -param pPolicyData [in]

A pointer to a <a href="https://msdn.microsoft.com/407de671-f6e3-407e-9c97-11ea9ac8bdde">WTS_POLICY_DATA</a> structure that contains the merged Group Policy values.


### -param pClientData [in, out]

A pointer to a <a href="https://msdn.microsoft.com/be2f7338-44a8-433f-b45d-620b9b7e93c7">WTS_USER_DATA</a> structure that contains client property information.


## -remarks



The Remote Desktop Services service merges all policy data, including listener settings, client-provided data, and Group Policy data, before calling this method.




## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

