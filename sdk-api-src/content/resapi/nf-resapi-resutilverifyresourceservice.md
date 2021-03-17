---
UID: NF:resapi.ResUtilVerifyResourceService
title: ResUtilVerifyResourceService function (resapi.h)
description: Verifies that a named service is starting or currently running. The PRESUTIL_VERIFY_RESOURCE_SERVICE type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_VERIFY_RESOURCE_SERVICE","PRESUTIL_VERIFY_RESOURCE_SERVICE function [Failover Cluster]","ResUtilVerifyResourceService","ResUtilVerifyResourceService function [Failover Cluster]","_wolf_resutilverifyresourceservice","mscs.resutilverifyresourceservice","resapi/PRESUTIL_VERIFY_RESOURCE_SERVICE","resapi/ResUtilVerifyResourceService"]
old-location: mscs\resutilverifyresourceservice.htm
tech.root: MsCS
ms.assetid: 452f4e83-74a6-4830-b244-599e9dc5c854
ms.date: 12/05/2018
ms.keywords: PRESUTIL_VERIFY_RESOURCE_SERVICE, PRESUTIL_VERIFY_RESOURCE_SERVICE function [Failover Cluster], ResUtilVerifyResourceService, ResUtilVerifyResourceService function [Failover Cluster], _wolf_resutilverifyresourceservice, mscs.resutilverifyresourceservice, resapi/PRESUTIL_VERIFY_RESOURCE_SERVICE, resapi/ResUtilVerifyResourceService
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
 - ResUtilVerifyResourceService
 - resapi/ResUtilVerifyResourceService
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
 - ResUtilVerifyResourceService
---

# ResUtilVerifyResourceService function


## -description

Verifies that a named <a href="/previous-versions/windows/desktop/mscs/s-gly">service</a> is starting or currently running. The <b>PRESUTIL_VERIFY_RESOURCE_SERVICE</b> type defines a pointer to this function.

## -parameters

### -param pszServiceName [in]

Null-terminated Unicode string containing the name of the service to verify.

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
<dt><b>ERROR_SERVICE_NOT_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The service is not operational.

</td>
</tr>
</table>