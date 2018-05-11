---
UID: NF:wtsprotocol.IWRdsRemoteFXGraphicsConnection.GetVirtualChannelTransport
title: IWRdsRemoteFXGraphicsConnection::GetVirtualChannelTransport
author: windows-driver-content
description: Retrieves the virtual channel transport object.
old-location: termserv\iwrdsremotefxgraphicsconnection_getvirtualchanneltransport.htm
old-project: TermServ
ms.assetid: 70de545f-f630-40cc-8456-ea0703caba17
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetVirtualChannelTransport, GetVirtualChannelTransport method [Remote Desktop Services], GetVirtualChannelTransport method [Remote Desktop Services],IWRdsRemoteFXGraphicsConnection interface, IWRdsRemoteFXGraphicsConnection interface [Remote Desktop Services],GetVirtualChannelTransport method, IWRdsRemoteFXGraphicsConnection.GetVirtualChannelTransport, IWRdsRemoteFXGraphicsConnection::GetVirtualChannelTransport, termserv.iwrdsremotefxgraphicsconnection_getvirtualchanneltransport, wtsprotocol/IWRdsRemoteFXGraphicsConnection::GetVirtualChannelTransport
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
-	IWRdsRemoteFXGraphicsConnection.GetVirtualChannelTransport
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsRemoteFXGraphicsConnection::GetVirtualChannelTransport


## -description


Retrieves the virtual channel transport object.


## -parameters




### -param ppTransport [out]

A pointer to a returned object pointer that represents the virtual channel transport. This is a pointer to the <a href="https://msdn.microsoft.com/629589cb-9879-491d-a224-6ae2ce8b0ea3">IWRdsGraphicsChannelManager</a> interface.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/ff8d2dd0-adbb-40de-a074-3228d803f4c8">IWRdsRemoteFXGraphicsConnection</a>
 

 

