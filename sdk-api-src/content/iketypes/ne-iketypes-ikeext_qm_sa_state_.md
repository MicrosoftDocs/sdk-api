---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IKEEXT_QM_SA_STATE_ enumeration


## -description


The <b>IKEEXT_QM_SA_STATE</b> enumerated type defines the states for the Quick Mode (QM) negotiation exchanges that are part of the Authenticated Internet Protocol (AuthIP) and Internet Key Exchange (IKE) protocols.


## -enum-fields




### -field IKEEXT_QM_SA_STATE_NONE

Initial state.  No QM packets have been sent to the peer.


### -field IKEEXT_QM_SA_STATE_INITIAL

First packet has been sent to the peer.


### -field IKEEXT_QM_SA_STATE_FINAL

Final packet has been sent to the peer.


### -field IKEEXT_QM_SA_STATE_COMPLETE

QM has been completed.


### -field IKEEXT_QM_SA_STATE_MAX

Maximum value for testing purposes.


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=94617">Quick Mode Negotiation</a>



<a href="https://msdn.microsoft.com/39029412-18ce-426a-a79d-cf25ff0dfe0d">Windows Filtering Platform API Enumerated Types</a>
 

 

