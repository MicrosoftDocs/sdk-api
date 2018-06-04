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

# _TRANSPORTCLIENT_CALLBACK_ID enumeration


## -description


This enumeration is received  by the <a href="https://msdn.microsoft.com/e3c809c4-5681-4979-8633-bb8d3dbde35b">WdsTransportClientRegisterCallback</a> function.


## -enum-fields




### -field WDS_TRANSPORTCLIENT_SESSION_START

Identifies the <a href="https://msdn.microsoft.com/47a053e3-f457-4d0a-80a8-1b93d5e8688f">PFN_WdsTransportClientSessionStart</a> callback.


### -field WDS_TRANSPORTCLIENT_RECEIVE_CONTENTS

Identifies the <a href="https://msdn.microsoft.com/3a1cd9bb-c0da-4d66-9338-1f284fc15499">PFN_WdsTransportClientReceiveContents</a> callback.


### -field WDS_TRANSPORTCLIENT_SESSION_COMPLETE

Identifies the <a href="https://msdn.microsoft.com/1c7b8137-bf74-486c-a90e-6becfec5ddc8">PFN_WdsTransportClientSessionComplete</a> callback.


### -field WDS_TRANSPORTCLIENT_RECEIVE_METADATA

Identifies the <a href="https://msdn.microsoft.com/9acde77b-5360-4c55-b11d-bf85e5c8d00e">PFN_WdsTransportClientReceiveMetadata</a> callback.


### -field WDS_TRANSPORTCLIENT_SESSION_STARTEX

Identifies the <a href="https://msdn.microsoft.com/36970f1b-9dbf-421f-a078-3da3bbb050e8">PFN_WdsTransportClientSessionStartEx</a> callback.


### -field WDS_TRANSPORTCLIENT_SESSION_NEGOTIATE


### -field WDS_TRANSPORTCLIENT_MAX_CALLBACKS

Used for validation checking.

