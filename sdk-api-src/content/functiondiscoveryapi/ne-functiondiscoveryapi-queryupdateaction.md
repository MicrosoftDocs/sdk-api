---
UID: NE:functiondiscoveryapi.tagQueryUpdateAction
title: QueryUpdateAction (functiondiscoveryapi.h)
author: windows-sdk-content
description: Represents the type of action Function Discovery is performing on the specified function instance. This information is used by the client program's change notification handler.
old-location: ncd\queryupdateaction_enum.htm
tech.root: FunDisc
ms.assetid: ae3a4fe2-1b1f-4a8d-9b5d-361a7ece315d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: QUA_ADD, QUA_CHANGE, QUA_REMOVE, QueryUpdateAction, QueryUpdateAction enumeration, functiondiscoveryapi/QUA_ADD, functiondiscoveryapi/QUA_CHANGE, functiondiscoveryapi/QUA_REMOVE, functiondiscoveryapi/QueryUpdateAction, ncd.queryupdateaction_enum
ms.topic: enum
req.header: functiondiscoveryapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryAPI.idl
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
 - HeaderDef
api_location:
 - FunctionDiscoveryAPI.h
api_name:
 - QueryUpdateAction
product: Windows
targetos: Windows
req.typenames: QueryUpdateAction
req.redist: 
ms.custom: 19H1
---

# QueryUpdateAction enumeration


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Represents the type of action Function Discovery is performing on the specified function instance. This information is used by the client program's change notification handler.


## -enum-fields




### -field QUA_ADD

Function Discovery is adding the specified function instance.


### -field QUA_REMOVE

Function Discovery is removing the specified function instance.


### -field QUA_CHANGE

Function Discovery is modifying the specified function instance.


## -remarks



When a client program implements the <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> interface and passes the address of the interface to one of the Query methods, Function Discovery calls the client program's <a href="https://msdn.microsoft.com/ab4d0fc6-de3f-49cf-b53c-573222a8bc89">IFunctionDiscoveryNotification::OnUpdate</a> method to notify the client program when a function instance which meets the query parameters has been added, removed, or modified.



