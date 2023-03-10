---
UID: NF:resapi.ResUtilStartResourceService
title: ResUtilStartResourceService function (resapi.h)
description: Starts a service. The PRESUTIL_START_RESOURCE_SERVICE type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_START_RESOURCE_SERVICE","PRESUTIL_START_RESOURCE_SERVICE function [Failover Cluster]","ResUtilStartResourceService","ResUtilStartResourceService function [Failover Cluster]","_wolf_resutilstartresourceservice","mscs.resutilstartresourceservice","resapi/PRESUTIL_START_RESOURCE_SERVICE","resapi/ResUtilStartResourceService"]
old-location: mscs\resutilstartresourceservice.htm
tech.root: MsCS
ms.assetid: 0c8a80d7-0291-4ed5-af44-67c0c251dc84
ms.date: 12/05/2018
ms.keywords: PRESUTIL_START_RESOURCE_SERVICE, PRESUTIL_START_RESOURCE_SERVICE function [Failover Cluster], ResUtilStartResourceService, ResUtilStartResourceService function [Failover Cluster], _wolf_resutilstartresourceservice, mscs.resutilstartresourceservice, resapi/PRESUTIL_START_RESOURCE_SERVICE, resapi/ResUtilStartResourceService
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
 - ResUtilStartResourceService
 - resapi/ResUtilStartResourceService
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
 - ResUtilStartResourceService
---

# ResUtilStartResourceService function


## -description

Starts a <a href="/previous-versions/windows/desktop/mscs/s-gly">service</a>. The <b>PRESUTIL_START_RESOURCE_SERVICE</b> type defines a pointer to this function.

## -parameters

### -param pszServiceName [in]

Null-terminated Unicode string containing the name of the service to start.

### -param phServiceHandle [out]

Optional pointer to a handle in which the handle to the started service is returned. This handle must be closed either by a call to the cluster utility function  <a href="/windows/desktop/api/resapi/nf-resapi-resutilstopservice">ResUtilStopService</a> or the function  <a href="/windows/desktop/api/winsvc/nf-winsvc-closeservicehandle">CloseServiceHandle</a>.

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
<dt><b>ERROR_SERVICE_NEVER_STARTED</b></dt>
</dl>
</td>
<td width="60%">
The service was not started.

</td>
</tr>
</table>

## -remarks

The  <b>ResUtilStartResourceService</b> utility function encapsulates the necessary calls to the service control manager, providing a convenient way to start services in the <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>. Using  <b>ResUtilStartResourceService</b> is optional. If the service to be started requires specific access restrictions or other special handling, use the service control manager functions instead.

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-resutilstopservice">ResUtilStopService</a>