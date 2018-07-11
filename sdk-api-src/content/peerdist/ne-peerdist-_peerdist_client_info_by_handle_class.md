---
UID: NE:peerdist._PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
title: "_PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS"
author: windows-sdk-content
description: The PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS enumeration defines the possible client information values.
old-location: p2p\peerdist_client_info_by_handle_class.htm
old-project: p2psdk
ms.assetid: 28391dc5-ec89-44d9-acac-b7ff3868e542
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: "*PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, MaximumPeerDistClientInfoByHandlesClass, PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS enumeration [Peer Networking], PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS enumeration pointer [Peer Networking], PeerDistClientBasicInfo, _PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, p2p.peerdist_client_info_by_handle_class, peerdist/MaximumPeerDistClientInfoByHandlesClass, peerdist/PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, peerdist/PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, peerdist/PeerDistClientBasicInfo"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: peerdist.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, *PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - peerdist.h
api_name:
 - PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS enumeration


## -description


The <b>PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS</b> enumeration defines the possible client information values.


## -enum-fields




### -field PeerDistClientBasicInfo

 Indicates the information to retrieve is a <a href="https://msdn.microsoft.com/abd98a28-b208-4f31-a28b-ff6ff6677af9">PEERDIST_CLIENT_BASIC_INFO</a> structure.


### -field MaximumPeerDistClientInfoByHandlesClass

The maximum value for the enumeration that is used for error checking.  This value should not be sent to the <a href="https://msdn.microsoft.com/d3bb080c-cde7-4623-95fd-3cffb3bd93aa">PeerDistClientGetInformationByHandle</a> function.


## -remarks



A value from this enumeration is passed to the<a href="https://msdn.microsoft.com/d3bb080c-cde7-4623-95fd-3cffb3bd93aa">PeerDistClientGetInformationByHandle</a> function as the <i>PeerDistClientInfoClass</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/d3bb080c-cde7-4623-95fd-3cffb3bd93aa">PeerDistClientGetInformationByHandle</a>
 

 

