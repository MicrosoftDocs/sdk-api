---
UID: NF:resapi.ResUtilIsPathValid
title: ResUtilIsPathValid function
author: windows-sdk-content
description: Checks whether a path is syntactically valid.
old-location: mscs\resutilispathvalid.htm
old-project: mscs
ms.assetid: 4cc8e0ad-8dbc-409d-b063-9fa26f810aac
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PRESUTIL_IS_PATH_VALID, PRESUTIL_IS_PATH_VALID function [Failover Cluster], ResUtilIsPathValid, ResUtilIsPathValid function [Failover Cluster], _wolf_resutilispathvalid, mscs.resutilispathvalid, resapi/PRESUTIL_IS_PATH_VALID, resapi/ResUtilIsPathValid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: resapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RESOURCE_EXIT_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilIsPathValid
product: Windows
targetos: Windows
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
req.product: ADAM
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



