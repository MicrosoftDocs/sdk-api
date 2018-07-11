---
UID: NC:resapi.PRESUTIL_IS_PATH_VALID
title: PRESUTIL_IS_PATH_VALID
author: windows-sdk-content
description: Checks whether a path is syntactically valid.
old-location: mscs\resutilispathvalid.htm
old-project: mscs
ms.assetid: 4cc8e0ad-8dbc-409d-b063-9fa26f810aac
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PRESUTIL_IS_PATH_VALID, PRESUTIL_IS_PATH_VALID callback, PRESUTIL_IS_PATH_VALID callback function [Failover Cluster], _wolf_resutilispathvalid, mscs.resutilispathvalid, resapi/PRESUTIL_IS_PATH_VALID
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - PRESUTIL_IS_PATH_VALID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PRESUTIL_IS_PATH_VALID callback function


## -description


Checks whether a path is syntactically valid.


## -parameters




### -param pszPath [in]

Pointer to the path to check.


## -returns



If the operation succeeds, the function returns <b>TRUE</b> and <i>pszPath</i> is valid.

If the operation fails, 
the function returns <b>FALSE</b>.



