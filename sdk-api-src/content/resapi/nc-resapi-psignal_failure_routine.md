---
UID: NC:resapi.PSIGNAL_FAILURE_ROUTINE
title: PSIGNAL_FAILURE_ROUTINE (resapi.h)
description: Reports that there was a failure in a resource instance. The PSIGNAL_FAILURE_ROUTINE type defines a pointer to this function.
helpviewer_keywords: ["PSIGNAL_FAILURE_ROUTINE","PSIGNAL_FAILURE_ROUTINE callback function [Failover Cluster]","SignalFailure","SignalFailure callback","SignalFailure callback function [Failover Cluster]","mscs.signalfailure","resapi/PSIGNAL_FAILURE_ROUTINE","resapi/SignalFailure"]
old-location: mscs\signalfailure.htm
tech.root: MsCS
ms.assetid: C4226174-B983-4BF5-8DA5-638201124037
ms.date: 12/05/2018
ms.keywords: PSIGNAL_FAILURE_ROUTINE, PSIGNAL_FAILURE_ROUTINE callback function [Failover Cluster], SignalFailure, SignalFailure callback, SignalFailure callback function [Failover Cluster], mscs.signalfailure, resapi/PSIGNAL_FAILURE_ROUTINE, resapi/SignalFailure
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSIGNAL_FAILURE_ROUTINE
 - resapi/PSIGNAL_FAILURE_ROUTINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - SignalFailure
---

# PSIGNAL_FAILURE_ROUTINE callback function


## -description

Reports that there was a failure in a resource instance. The <b>PSIGNAL_FAILURE_ROUTINE</b> type defines a pointer to this function.

## -parameters

### -param ResourceHandle [in]

A handle to the resource instance.

### -param FailureType [in]

A <a href="/windows/desktop/api/resapi/ne-resapi-failure_type">FAILURE_TYPE</a> enumeration value that describes the failure type.

<b>Windows Server 2012:  </b>Not supported.

### -param ApplicationSpecificErrorCode [in]

An application error code.


#### - IsEmbeddedFailure [in]

Not supported.

<b>Windows Server 2012:  </b><b>TRUE</b> if this failure is an embedded failure; otherwise <b>FALSE</b>.

## -returns

Returns <b>ERROR_SUCCESS</b> (0), if the operation succeeds; otherwise returns a system error code.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-callback-functions">Resource DLL Callback Functions</a>