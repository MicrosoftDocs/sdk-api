---
UID: NF:wtsprotocol.IWRdsRemoteFXGraphicsConnection.EnableRemoteFXGraphics
title: IWRdsRemoteFXGraphicsConnection::EnableRemoteFXGraphics
author: windows-driver-content
description: Queries the protocol if RemoteFX graphics should be enabled for the connection.
old-location: termserv\iwrdsremotefxgraphicsconnection_enableremotefxgraphics.htm
old-project: TermServ
ms.assetid: 3ad667ed-bbb5-44e2-992a-df90bbab7b79
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: EnableRemoteFXGraphics, EnableRemoteFXGraphics method [Remote Desktop Services], EnableRemoteFXGraphics method [Remote Desktop Services],IWRdsRemoteFXGraphicsConnection interface, IWRdsRemoteFXGraphicsConnection interface [Remote Desktop Services],EnableRemoteFXGraphics method, IWRdsRemoteFXGraphicsConnection.EnableRemoteFXGraphics, IWRdsRemoteFXGraphicsConnection::EnableRemoteFXGraphics, termserv.iwrdsremotefxgraphicsconnection_enableremotefxgraphics, wtsprotocol/IWRdsRemoteFXGraphicsConnection::EnableRemoteFXGraphics
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
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wtsprotocol.h
api_name:
-	IWRdsRemoteFXGraphicsConnection.EnableRemoteFXGraphics
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsRemoteFXGraphicsConnection::EnableRemoteFXGraphics


## -description


Queries the protocol if RemoteFX graphics should be enabled for the connection.


## -parameters




### -param pEnableRemoteFXGraphics [out]

The address of a <b>BOOL</b> variable that receives  <b>TRUE</b> to enable remote FX graphics; otherwise, <b>FALSE</b>.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/ff8d2dd0-adbb-40de-a074-3228d803f4c8">IWRdsRemoteFXGraphicsConnection</a>
 

 

