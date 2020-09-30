---
UID: NF:resapi.ResUtilIsPathValid
title: ResUtilIsPathValid function (resapi.h)
description: Checks whether a path is syntactically valid.
helpviewer_keywords: ["PRESUTIL_IS_PATH_VALID","PRESUTIL_IS_PATH_VALID function [Failover Cluster]","ResUtilIsPathValid","ResUtilIsPathValid function [Failover Cluster]","_wolf_resutilispathvalid","mscs.resutilispathvalid","resapi/PRESUTIL_IS_PATH_VALID","resapi/ResUtilIsPathValid"]
old-location: mscs\resutilispathvalid.htm
tech.root: MsCS
ms.assetid: 4cc8e0ad-8dbc-409d-b063-9fa26f810aac
ms.date: 12/05/2018
ms.keywords: PRESUTIL_IS_PATH_VALID, PRESUTIL_IS_PATH_VALID function [Failover Cluster], ResUtilIsPathValid, ResUtilIsPathValid function [Failover Cluster], _wolf_resutilispathvalid, mscs.resutilispathvalid, resapi/PRESUTIL_IS_PATH_VALID, resapi/ResUtilIsPathValid
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
 - ResUtilIsPathValid
 - resapi/ResUtilIsPathValid
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
 - ResUtilIsPathValid
---

# ResUtilIsPathValid function


## -description

Checks whether a path is syntactically valid.

## -parameters

### -param pszPath [in]

Pointer to the path to check.

## -returns

If the operation succeeds, the function returns <b>TRUE</b> and <i>pszPath</i> is valid.

If the operation fails, 
the function returns <b>FALSE</b>.

