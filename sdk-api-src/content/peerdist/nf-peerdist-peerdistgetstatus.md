---
UID: NF:peerdist.PeerDistGetStatus
title: PeerDistGetStatus function
author: windows-sdk-content
description: PeerDistGetStatus function returns the current status of the Peer Distribution service.
old-location: p2p\peerdistgetstatus.htm
old-project: P2PSdk
ms.assetid: 1ab188cc-db79-49b2-977f-0b8fccf7f274
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: PeerDistGetStatus, PeerDistGetStatus function [Peer Networking], p2p.peerdistgetstatus, peerdist/PeerDistGetStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: peerdist.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - DllExport
api_location:
 - PeerDist.dll
api_name:
 - PeerDistGetStatus
product: Windows
targetos: Windows
req.lib: PeerDist.lib
req.dll: PeerDist.dll
req.irql: 
req.product: ADAM
---

# PeerDistGetStatus function


## -description


The <b>PeerDistGetStatus</b> function returns the current status of the Peer Distribution service.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param pPeerDistStatus [out]

A pointer to a <a href="https://msdn.microsoft.com/d693dc1c-39ce-4a2b-b769-9d370abc3d3c">PEERDIST_STATUS</a> enumeration which upon operation success receives the current status of the Peer Distribution service.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -remarks



A Group Policy change can result in the Peer Distribution service  moving to an  available, unavailable, or disabled state. Depending on the resultant state of this transition, the content, content information, or stream handles  the caller has access to may  no longer function. If this is the case, the caller must explicitly close the handles by calling the appropriate Peer Distribution API.




## -see-also




<a href="https://msdn.microsoft.com/d693dc1c-39ce-4a2b-b769-9d370abc3d3c">PEERDIST_STATUS</a>



<a href="https://msdn.microsoft.com/c55300b7-13b6-42bf-b673-56a5e077416d">PeerDistClientCloseContent</a>



<a href="https://msdn.microsoft.com/066f1856-0617-40c7-a444-9765c01b4563">PeerDistServerCloseContentInformation</a>



<a href="https://msdn.microsoft.com/599b4694-3d03-4d25-9d02-313599aaaf0b">PeerDistServerCloseStreamHandle</a>
 

 

