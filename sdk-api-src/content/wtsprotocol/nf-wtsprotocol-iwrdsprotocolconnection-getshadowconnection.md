---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetShadowConnection
title: IWRdsProtocolConnection::GetShadowConnection
author: windows-sdk-content
description: Retrieves a reference to the shadow connection object from the protocol.
old-location: termserv\iwrdsprotocolconnection_getshadowconnection.htm
tech.root: TermServ
ms.assetid: 1b1059af-f673-47fd-85fc-57df76adfbcf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetShadowConnection, GetShadowConnection method [Remote Desktop Services], GetShadowConnection method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetShadowConnection method, IWRdsProtocolConnection.GetShadowConnection, IWRdsProtocolConnection::GetShadowConnection, termserv.iwrdsprotocolconnection_getshadowconnection, wtsprotocol/IWRdsProtocolConnection::GetShadowConnection
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
 - IWRdsProtocolConnection.GetShadowConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolConnection::GetShadowConnection


## -description


Retrieves a reference to the shadow connection object from the protocol.


## -parameters




### -param ppShadowConnection [out]

The address of <a href="https://msdn.microsoft.com/d23c4902-4e61-45ff-8a49-62eea1b92d4a">IWRdsProtocolShadowConnection</a> interface pointer that receives the reference to the shadow connection object. This method must add a reference to the object before returning. When the Remote Desktop Services service no longer needs the object, it will release it.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a>



<a href="https://msdn.microsoft.com/d23c4902-4e61-45ff-8a49-62eea1b92d4a">IWRdsProtocolShadowConnection</a>
 

 

