---
UID: NC:resapi.PCANCEL_ROUTINE
title: PCANCEL_ROUTINE (resapi.h)
author: windows-sdk-content
description: Cancels an operation on a resource.
old-location: mscs\cancel.htm
tech.root: MsCS
ms.assetid: F2A22C00-5B25-48F7-BB25-9C351A47B770
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel callback, Cancel callback function [Failover Cluster], PCANCEL_ROUTINE, PCANCEL_ROUTINE callback function [Failover Cluster], mscs.cancel, resapi/Cancel, resapi/PCANCEL_ROUTINE
ms.topic: callback
f1_keywords: 
 - "resapi/Cancel"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - Cancel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PCANCEL_ROUTINE callback function


## -description


Cancels an operation on a resource.


## -parameters




### -param Resource [in]

The resource ID of the resource.


### -param CancelFlags_RESERVED [in]

Reserved.


## -returns



<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The quorum resource was successfully released and is no longer being defended.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/msipc/error-codes">Error code</a></b></dt>
</dl>
</td>
<td width="60%">
The operation was not successfully canceled.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-dll-entry-point-functions">Resource DLL Entry-Point Functions</a>
 

 

