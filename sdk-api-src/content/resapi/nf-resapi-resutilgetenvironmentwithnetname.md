---
UID: NF:resapi.ResUtilGetEnvironmentWithNetName
title: ResUtilGetEnvironmentWithNetName function (resapi.h)
description: Adjusts environment data for a resource so that the resource uses a cluster network name to identify its location.
helpviewer_keywords: ["PRESUTIL_GET_ENVIRONMENT_WITH_NET_NAME","PRESUTIL_GET_ENVIRONMENT_WITH_NET_NAME function [Failover Cluster]","ResUtilGetEnvironmentWithNetName","ResUtilGetEnvironmentWithNetName function [Failover Cluster]","_wolf_resutilgetenvironmentwithnetname","mscs.resutilgetenvironmentwithnetname","resapi/PRESUTIL_GET_ENVIRONMENT_WITH_NET_NAME","resapi/ResUtilGetEnvironmentWithNetName"]
old-location: mscs\resutilgetenvironmentwithnetname.htm
tech.root: MsCS
ms.assetid: 683235ac-153d-4442-915e-e1bf9b5e8810
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_ENVIRONMENT_WITH_NET_NAME, PRESUTIL_GET_ENVIRONMENT_WITH_NET_NAME function [Failover Cluster], ResUtilGetEnvironmentWithNetName, ResUtilGetEnvironmentWithNetName function [Failover Cluster], _wolf_resutilgetenvironmentwithnetname, mscs.resutilgetenvironmentwithnetname, resapi/PRESUTIL_GET_ENVIRONMENT_WITH_NET_NAME, resapi/ResUtilGetEnvironmentWithNetName
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
 - ResUtilGetEnvironmentWithNetName
 - resapi/ResUtilGetEnvironmentWithNetName
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
 - ResUtilGetEnvironmentWithNetName
---

# ResUtilGetEnvironmentWithNetName function


## -description

Adjusts environment data for a  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> so that the resource uses a cluster network name to identify its location. The resource must be dependent on a  <a href="/previous-versions/windows/desktop/mscs/network-name">Network Name</a> resource. The <b>PRESUTIL_GET_ENVIRONMENT_WITH_NET_NAME</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Handle to a resource that depends on a Network Name resource.

## -returns

If the operations succeeds, the function returns a pointer to the environment block.

If the operation fails, 
the function returns <b>NULL</b>. For more information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The  <b>ResUtilGetEnvironmentWithNetName</b> function appends environment variables to the current environment block. Pass the returned environment block to  <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> when starting the resource to achieve the following effects:

<ul>
<li>Clients and the <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> can locate the resource by using the name of the Network Name resource.</li>
<li>If the resource calls <a href="/windows/desktop/api/winbase/nf-winbase-getcomputernamea">GetComputerName</a>, <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa">GetComputerNameEx</a>, or <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname">gethostbyname</a>, the network name will be returned regardless of which node is currently hosting the resource.</li>
</ul>
If the resource identified by <i>hResource</i> is not dependent on a Network Name resource,  <b>ResUtilGetEnvironmentWithNetName</b> returns <b>NULL</b>.

Use  <a href="/windows/desktop/api/resapi/nf-resapi-resutilfreeenvironment">ResUtilFreeEnvironment</a> to destroy the environment block.

Do not call  <b>ResUtilGetEnvironmentWithNetName</b> from any resource DLL entry point function.  <b>ResUtilGetEnvironmentWithNetName</b> can safely be called from a worker thread. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetresourceserviceenvironment">ResUtilSetResourceServiceEnvironment</a>