---
UID: NF:resapi.ResUtilFreeEnvironment
title: ResUtilFreeEnvironment function (resapi.h)
description: Destroys the environment variable block created with ResUtilGetEnvironmentWithNetName. The PRESUTIL_FREE_ENVIRONMENT type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_FREE_ENVIRONMENT","PRESUTIL_FREE_ENVIRONMENT function [Failover Cluster]","ResUtilFreeEnvironment","ResUtilFreeEnvironment function [Failover Cluster]","_wolf_resutilfreeenvironment","mscs.resutilfreeenvironment","resapi/PRESUTIL_FREE_ENVIRONMENT","resapi/ResUtilFreeEnvironment"]
old-location: mscs\resutilfreeenvironment.htm
tech.root: MsCS
ms.assetid: 196f347e-2b2f-4bb1-a86c-b2a73881ed65
ms.date: 12/05/2018
ms.keywords: PRESUTIL_FREE_ENVIRONMENT, PRESUTIL_FREE_ENVIRONMENT function [Failover Cluster], ResUtilFreeEnvironment, ResUtilFreeEnvironment function [Failover Cluster], _wolf_resutilfreeenvironment, mscs.resutilfreeenvironment, resapi/PRESUTIL_FREE_ENVIRONMENT, resapi/ResUtilFreeEnvironment
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
 - ResUtilFreeEnvironment
 - resapi/ResUtilFreeEnvironment
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
 - ResUtilFreeEnvironment
---

# ResUtilFreeEnvironment function


## -description

Destroys the environment variable block created with  <a href="/windows/desktop/api/resapi/nf-resapi-resutilgetenvironmentwithnetname">ResUtilGetEnvironmentWithNetName</a>. The <b>PRESUTIL_FREE_ENVIRONMENT</b> type defines a pointer to this function.

## -parameters

### -param lpEnvironment [in]

Pointer to the environment variable block returned from  <a href="/windows/desktop/api/resapi/nf-resapi-resutilgetenvironmentwithnetname">ResUtilGetEnvironmentWithNetName</a>.

## -returns

This function has no return values.

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetenvironmentwithnetname">ResUtilGetEnvironmentWithNetName</a>