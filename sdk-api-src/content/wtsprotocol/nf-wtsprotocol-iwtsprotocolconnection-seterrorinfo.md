---
UID: NF:wtsprotocol.IWTSProtocolConnection.SetErrorInfo
title: IWTSProtocolConnection::SetErrorInfo
author: windows-driver-content
description: IWTSProtocolConnection::SetErrorInfo is no longer available. Instead, use IWRdsProtocolConnection::SetErrorInfo.
old-location: termserv\iwtsprotocolconnection_seterrorinfo.htm
old-project: TermServ
ms.assetid: 0ec35560-5aad-403a-9477-50e48ee7136a
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IWTSProtocolConnection interface [Remote Desktop Services],SetErrorInfo method, IWTSProtocolConnection.SetErrorInfo, IWTSProtocolConnection::SetErrorInfo, SetErrorInfo, SetErrorInfo method [Remote Desktop Services], SetErrorInfo method [Remote Desktop Services],IWTSProtocolConnection interface, termserv.iwtsprotocolconnection_seterrorinfo, wtsprotocol/IWTSProtocolConnection::SetErrorInfo
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
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wtsprotocol.h
api_name:
-	IWTSProtocolConnection.SetErrorInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolConnection::SetErrorInfo


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::SetErrorInfo</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/114abaf1-fe67-4d80-ad5d-f49aac9dd587">IWRdsProtocolConnection::SetErrorInfo</a>.]

Sends an error code to the client.


## -parameters




### -param ulError [in]

An integer that contains the error code.


## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

