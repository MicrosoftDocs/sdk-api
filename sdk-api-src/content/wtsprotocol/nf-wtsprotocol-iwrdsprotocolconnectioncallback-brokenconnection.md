---
UID: NF:wtsprotocol.IWRdsProtocolConnectionCallback.BrokenConnection
title: IWRdsProtocolConnectionCallback::BrokenConnection
author: windows-sdk-content
description: Informs the Remote Desktop Services service that the client connection has been lost.
old-location: termserv\iwrdsprotocolconnectioncallback_brokenconnection.htm
tech.root: termserv
ms.assetid: bc317e10-e09c-423b-8016-eb1cf49eba43
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: BrokenConnection, BrokenConnection method [Remote Desktop Services], BrokenConnection method [Remote Desktop Services],IWRdsProtocolConnectionCallback interface, IWRdsProtocolConnectionCallback interface [Remote Desktop Services],BrokenConnection method, IWRdsProtocolConnectionCallback.BrokenConnection, IWRdsProtocolConnectionCallback::BrokenConnection, termserv.iwrdsprotocolconnectioncallback_brokenconnection, wtsprotocol/IWRdsProtocolConnectionCallback::BrokenConnection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolConnectionCallback.BrokenConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolConnectionCallback::BrokenConnection


## -description


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




<a href="https://msdn.microsoft.com/81a73688-f39e-4960-8587-602d56c11e7e">IWRdsProtocolConnectionCallback</a>
 

 

