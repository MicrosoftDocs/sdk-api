---
UID: NC:resapi.PRELEASE_ROUTINE
title: PRELEASE_ROUTINE (resapi.h)
author: windows-sdk-content
description: Releases the quorum resource from arbitration.
old-location: mscs\release.htm
tech.root: MsCS
ms.assetid: 9e8e4557-b223-4f8f-9393-67f589181754
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PRELEASE_ROUTINE, PRELEASE_ROUTINE callback, Release, Release callback function [Failover Cluster], _wolf_release, mscs.release, resapi/PRELEASE_ROUTINE, resapi/Release
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
 - Release
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PRELEASE_ROUTINE callback function


## -description


Releases the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/quorum-resource">quorum resource</a> from arbitration. The 
    <b>PCLOSE_ROUTINE</b> type defines a pointer to this function.


## -parameters




### -param Resource [in]

Resource identifier for the quorum resource to be released.


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
<dt><b><a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">Error code</a></b></dt>
</dl>
</td>
<td width="60%">
The quorum resource was not successfully released.

</td>
</tr>
</table>
 




## -remarks



The <i>Release</i> entry-point function is implemented for quorum 
     resources only. A quorum resource might have to be released when the 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a> is shut down or when the quorum resource 
     has to be physically moved to a different <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/nodes">node</a> in the cluster.

<div class="alert"><b>Note</b>  All disk resources must explicitly call their own 
    <i>Release</i> in their  implementation of the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a> callback, since one is not made by the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-monitor">Resource Monitor</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-dll-entry-point-functions">Resource DLL Entry-Point Functions</a>
 

 

