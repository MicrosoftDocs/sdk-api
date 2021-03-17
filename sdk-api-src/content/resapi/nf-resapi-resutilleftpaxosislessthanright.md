---
UID: NF:resapi.ResUtilLeftPaxosIsLessThanRight
title: ResUtilLeftPaxosIsLessThanRight function (resapi.h)
description: Indicates whether a specified Paxos tag contains older cluster configuration information than another specified Paxos tag.
helpviewer_keywords: ["ResUtilLeftPaxosIsLessThanRight","ResUtilLeftPaxosIsLessThanRight function [Failover Cluster]","mscs.resutilleftpaxosislessthanright","resapi/ResUtilLeftPaxosIsLessThanRight"]
old-location: mscs\resutilleftpaxosislessthanright.htm
tech.root: MsCS
ms.assetid: 01CBFC67-02D0-439D-BE4E-EA0A2448FDEE
ms.date: 12/05/2018
ms.keywords: ResUtilLeftPaxosIsLessThanRight, ResUtilLeftPaxosIsLessThanRight function [Failover Cluster], mscs.resutilleftpaxosislessthanright, resapi/ResUtilLeftPaxosIsLessThanRight
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResUtilLeftPaxosIsLessThanRight
 - resapi/ResUtilLeftPaxosIsLessThanRight
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilLeftPaxosIsLessThanRight
---

# ResUtilLeftPaxosIsLessThanRight function


## -description

Indicates whether a specified Paxos tag contains older cluster configuration information than another specified Paxos tag.

## -parameters

### -param left [in]

The <a href="/windows/desktop/api/resapi/ns-resapi-paxostagcstruct">PaxosTagCStruct</a> structure that represents the first Paxos tag to use in the comparison.

### -param right [in]

The <a href="/windows/desktop/api/resapi/ns-resapi-paxostagcstruct">PaxosTagCStruct</a> structure that represents the 2nd  Paxos tag to use in the comparison.

## -returns

<b>TRUE</b> if the cluster configuration of the first Paxos tag is older than the that of the second Paxos tag; otherwise <b>FALSE</b>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-utility-functions">Resource Utility Functions</a>