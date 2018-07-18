---
UID: NS:peerdist._PEERDIST_CLIENT_BASIC_INFO
title: "_PEERDIST_CLIENT_BASIC_INFO"
author: windows-sdk-content
description: The PEERDIST_CLIENT_BASIC_INFO structure indicates whether or not there are many clients simultaneously downloading the same content.
old-location: p2p\peerdist_client_basic_info.htm
old-project: P2PSdk
ms.assetid: abd98a28-b208-4f31-a28b-ff6ff6677af9
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*PPEERDIST_CLIENT_BASIC_INFO, PEERDIST_CLIENT_BASIC_INFO, PEERDIST_CLIENT_BASIC_INFO structure [Peer Networking], PPEERDIST_CLIENT_BASIC_INFO, PPEERDIST_CLIENT_BASIC_INFO structure pointer [Peer Networking], _PEERDIST_CLIENT_BASIC_INFO, p2p.peerdist_client_basic_info, peerdist/PEERDIST_CLIENT_BASIC_INFO, peerdist/PPEERDIST_CLIENT_BASIC_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: PEERDIST_CLIENT_BASIC_INFO, *PPEERDIST_CLIENT_BASIC_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - peerdist.h
api_name:
 - PEERDIST_CLIENT_BASIC_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _PEERDIST_CLIENT_BASIC_INFO structure


## -description


The <b>PEERDIST_CLIENT_BASIC_INFO</b> structure indicates whether or not there are many clients simultaneously downloading the same content.


## -struct-fields




### -field fFlashCrowd

Indicates that a "flash crowd" situation has been detected, where many clients in the branch office are simultaneously downloading the same content.  


## -remarks



Thie <b>PEERDIST_CLIENT_BASIC_INFO</b> structure is retrieved from the <a href="https://msdn.microsoft.com/d3bb080c-cde7-4623-95fd-3cffb3bd93aa">PeerDistClientGetInformationHandle</a> function with PeerDistClientBasicInfo value specified for the <i>PeerDistClientInfoClass</i> parameter.

If true,  content that cannot be retrieved from the Peer Distribution APIs may soon be available for retrieval.




## -see-also




<a href="https://msdn.microsoft.com/d3bb080c-cde7-4623-95fd-3cffb3bd93aa">PeerDistClientGetInformationHandle</a>
 

 

