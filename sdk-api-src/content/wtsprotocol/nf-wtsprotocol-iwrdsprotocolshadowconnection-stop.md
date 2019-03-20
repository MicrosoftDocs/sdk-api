---
UID: NF:wtsprotocol.IWRdsProtocolShadowConnection.Stop
title: IWRdsProtocolShadowConnection::Stop (wtsprotocol.h)
author: windows-sdk-content
description: Notifies the protocol that shadowing has stopped.
old-location: termserv\iwrdsprotocolshadowconnection_stop.htm
tech.root: TermServ
ms.assetid: b6abe698-a390-485a-9a31-823ff25351c2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWRdsProtocolShadowConnection interface [Remote Desktop Services],Stop method, IWRdsProtocolShadowConnection.Stop, IWRdsProtocolShadowConnection::Stop, Stop, Stop method [Remote Desktop Services], Stop method [Remote Desktop Services],IWRdsProtocolShadowConnection interface, termserv.iwrdsprotocolshadowconnection_stop, wtsprotocol/IWRdsProtocolShadowConnection::Stop
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
 - IWRdsProtocolShadowConnection.Stop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolShadowConnection::Stop


## -description


Notifies the protocol that shadowing has stopped.


## -parameters






## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. The Remote Desktop Services service drops the connection if an error is returned.




## -remarks



The Remote Desktop Services service also changes the session state on the shadowed client to reflect the fact it is no longer being shadowed.




## -see-also




<a href="https://msdn.microsoft.com/d23c4902-4e61-45ff-8a49-62eea1b92d4a">IWRdsProtocolShadowConnection</a>
 

 

