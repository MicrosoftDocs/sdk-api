---
UID: NF:wtsprotocol.IWRdsRemoteFXGraphicsConnection.GetVirtualChannelTransport
title: IWRdsRemoteFXGraphicsConnection::GetVirtualChannelTransport (wtsprotocol.h)
author: windows-sdk-content
description: Retrieves the virtual channel transport object.
old-location: termserv\iwrdsremotefxgraphicsconnection_getvirtualchanneltransport.htm
tech.root: TermServ
ms.assetid: 70de545f-f630-40cc-8456-ea0703caba17
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetVirtualChannelTransport, GetVirtualChannelTransport method [Remote Desktop Services], GetVirtualChannelTransport method [Remote Desktop Services],IWRdsRemoteFXGraphicsConnection interface, IWRdsRemoteFXGraphicsConnection interface [Remote Desktop Services],GetVirtualChannelTransport method, IWRdsRemoteFXGraphicsConnection.GetVirtualChannelTransport, IWRdsRemoteFXGraphicsConnection::GetVirtualChannelTransport, termserv.iwrdsremotefxgraphicsconnection_getvirtualchanneltransport, wtsprotocol/IWRdsRemoteFXGraphicsConnection::GetVirtualChannelTransport
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
 - IWRdsRemoteFXGraphicsConnection.GetVirtualChannelTransport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsRemoteFXGraphicsConnection::GetVirtualChannelTransport


## -description


<p class="CCE_Message">[The GetVirtualChannelTransport method is deprecated and should not be used.
]

Retrieves the virtual channel transport object.


## -parameters




### -param ppTransport [out]

A pointer to a returned object pointer that represents the virtual channel transport. This is a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nn-wrdsgraphicschannels-iwrdsgraphicschannelmanager">IWRdsGraphicsChannelManager</a> interface.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection">IWRdsRemoteFXGraphicsConnection</a>
 

 

