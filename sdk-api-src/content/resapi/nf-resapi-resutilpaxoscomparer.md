---
UID: NF:resapi.ResUtilPaxosComparer
title: ResUtilPaxosComparer function (resapi.h)
description: Compares two Paxos tags and indicates whether they have the same values.
helpviewer_keywords: ["ResUtilPaxosComparer","ResUtilPaxosComparer function [Failover Cluster]","mscs.resutilpaxoscomparer","resapi/ResUtilPaxosComparer"]
old-location: mscs\resutilpaxoscomparer.htm
tech.root: MsCS
ms.assetid: 414F9BB0-2490-43A9-BE38-877B283573E1
ms.date: 12/05/2018
ms.keywords: ResUtilPaxosComparer, ResUtilPaxosComparer function [Failover Cluster], mscs.resutilpaxoscomparer, resapi/ResUtilPaxosComparer
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
 - ResUtilPaxosComparer
 - resapi/ResUtilPaxosComparer
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
 - ResUtilPaxosComparer
---

# ResUtilPaxosComparer function


## -description

Compares two Paxos tags and indicates whether they have the same values.

## -parameters

### -param left [in]

The <a href="/windows/desktop/api/resapi/ns-resapi-paxostagcstruct">PaxosTagCStruct</a> structure that represents the first Paxos tag to use in the comparison.

### -param right [in]

The <a href="/windows/desktop/api/resapi/ns-resapi-paxostagcstruct">PaxosTagCStruct</a> structure that represents the second  Paxos tag to use in the comparison.

## -returns

<b>TRUE</b> if the Paxos tags have the same values; otherwise <b>FALSE</b>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-utility-functions">Resource Utility Functions</a>