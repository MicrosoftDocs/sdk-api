---
UID: NF:resapi.ResUtilStopResourceService
title: ResUtilStopResourceService function (resapi.h)
description: Stops a named service. The PRESUTIL_STOP_RESOURCE_SERVICE type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_STOP_RESOURCE_SERVICE","PRESUTIL_STOP_RESOURCE_SERVICE function [Failover Cluster]","ResUtilStopResourceService","ResUtilStopResourceService function [Failover Cluster]","_wolf_resutilstopresourceservice","mscs.resutilstopresourceservice","resapi/PRESUTIL_STOP_RESOURCE_SERVICE","resapi/ResUtilStopResourceService"]
old-location: mscs\resutilstopresourceservice.htm
tech.root: MsCS
ms.assetid: 25e8417d-d314-4987-bdb2-7740793e4ac2
ms.date: 12/05/2018
ms.keywords: PRESUTIL_STOP_RESOURCE_SERVICE, PRESUTIL_STOP_RESOURCE_SERVICE function [Failover Cluster], ResUtilStopResourceService, ResUtilStopResourceService function [Failover Cluster], _wolf_resutilstopresourceservice, mscs.resutilstopresourceservice, resapi/PRESUTIL_STOP_RESOURCE_SERVICE, resapi/ResUtilStopResourceService
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
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResUtilStopResourceService
 - resapi/ResUtilStopResourceService
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
 - ResUtilStopResourceService
---

# ResUtilStopResourceService function


## -description

Stops a named <a href="/previous-versions/windows/desktop/mscs/s-gly">service</a>. The <b>PRESUTIL_STOP_RESOURCE_SERVICE</b> type defines a pointer to this function.

## -parameters

### -param pszServiceName [in]

Null-terminated Unicode string containing the name of the service to stop.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following is a possible error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
Service did not stop after a reasonable number of retries.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-resutilstartresourceservice">ResUtilStartResourceService</a>