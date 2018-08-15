---
UID: NF:wtsprotocol.IWTSProtocolConnectionCallback.BrokenConnection
title: IWTSProtocolConnectionCallback::BrokenConnection
author: windows-sdk-content
description: IWTSProtocolConnectionCallback::BrokenConnection is no longer available. Instead, use IWRdsProtocolConnectionCallback::BrokenConnection.
old-location: termserv\iwtsprotocolconnectioncallback_brokenconnection.htm
old-project: termserv
ms.assetid: a5878289-9335-4b3b-b66a-4c168b868f87
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: BrokenConnection, BrokenConnection method [Remote Desktop Services], BrokenConnection method [Remote Desktop Services],IWTSProtocolConnectionCallback interface, IWTSProtocolConnectionCallback interface [Remote Desktop Services],BrokenConnection method, IWTSProtocolConnectionCallback.BrokenConnection, IWTSProtocolConnectionCallback::BrokenConnection, termserv.iwtsprotocolconnectioncallback_brokenconnection, wtsprotocol/IWTSProtocolConnectionCallback::BrokenConnection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolConnectionCallback.BrokenConnection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolConnectionCallback::BrokenConnection


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnectionCallback::BrokenConnection</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/bc317e10-e09c-423b-8016-eb1cf49eba43">IWRdsProtocolConnectionCallback::BrokenConnection</a>.]

Informs the Remote Desktop Services service that the client connection has been lost.


## -parameters




### -param Reason [in]

This parameter is not used.


### -param Source [in]

This parameter is not used.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/ac8a2a66-fa1f-48bd-9502-def833e26f31">IWTSProtocolConnectionCallback</a>
 

 

