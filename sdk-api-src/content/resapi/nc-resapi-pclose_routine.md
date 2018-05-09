---
UID: NC:resapi.PCLOSE_ROUTINE
title: PCLOSE_ROUTINE
author: windows-driver-content
description: Cancels an operation on a resource.
old-location: mscs\cancel.htm
old-project: MsCS
ms.assetid: F2A22C00-5B25-48F7-BB25-9C351A47B770
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: Cancel, Cancel callback, Cancel callback function [Failover Cluster], PCLOSE_ROUTINE, PCLOSE_ROUTINE callback function [Failover Cluster], mscs.cancel, resapi/Cancel, resapi/PCLOSE_ROUTINE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ResApi.h
api_name:
-	Cancel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PCLOSE_ROUTINE callback function


## -description


Cancels an operation on a resource.


## -parameters




### -param Resource [in]

The resource ID of the resource.


#### - CancelFlags_RESERVED [in]

Reserved.


## -returns





Returns VOID that ...






## -see-also




<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry-Point Functions</a>
 

 

