---
UID: NC:resapi.PSIGNAL_FAILURE_ROUTINE
title: PSIGNAL_FAILURE_ROUTINE
author: windows-sdk-content
description: Reports that there was a failure in a resource instance. The PSIGNAL_FAILURE_ROUTINE type defines a pointer to this function.
old-location: mscs\signalfailure.htm
old-project: mscs
ms.assetid: C4226174-B983-4BF5-8DA5-638201124037
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PSIGNAL_FAILURE_ROUTINE, PSIGNAL_FAILURE_ROUTINE callback function [Failover Cluster], SignalFailure, SignalFailure callback, SignalFailure callback function [Failover Cluster], mscs.signalfailure, resapi/PSIGNAL_FAILURE_ROUTINE, resapi/SignalFailure
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - SignalFailure
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PSIGNAL_FAILURE_ROUTINE callback function


## -description


Reports that there was a failure in a resource instance. The <b>PSIGNAL_FAILURE_ROUTINE</b> type defines a pointer to this function.


## -parameters




### -param ResourceHandle [in]

A handle to the resource instance.


### -param FailureType [in]

A <a href="https://msdn.microsoft.com/C838BE66-5CAB-4884-AC64-EC5EC3A87679">FAILURE_TYPE</a> enumeration value that describes the failure type.

<b>Windows Server 2012:  </b>Not supported.


### -param ApplicationSpecificErrorCode [in]

An application error code.


#### - IsEmbeddedFailure [in]

Not supported.

<b>Windows Server 2012:  </b><b>TRUE</b> if this failure is an embedded failure; otherwise <b>FALSE</b>.


## -returns



Returns <b>ERROR_SUCCESS</b> (0), if the operation succeeds; otherwise returns a system error code.




## -see-also




<a href="https://msdn.microsoft.com/6c7de7e6-a0f5-4308-8cf3-21968bd339a4">Resource DLL Callback Functions</a>
 

 

