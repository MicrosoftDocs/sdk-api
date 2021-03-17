---
UID: NF:sspi.SspiGetTargetHostName
title: SspiGetTargetHostName function (sspi.h)
description: Gets the host name associated with the specified target.
helpviewer_keywords: ["SspiGetTargetHostName","SspiGetTargetHostName function [Security]","security.sspigettargethostname","sspi/SspiGetTargetHostName"]
old-location: security\sspigettargethostname.htm
tech.root: security
ms.assetid: 84570dfc-1890-4b82-b411-1f9eaa75537b
ms.date: 12/05/2018
ms.keywords: SspiGetTargetHostName, SspiGetTargetHostName function [Security], security.sspigettargethostname, sspi/SspiGetTargetHostName
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Secur32.lib
req.dll: SspiCli.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SspiGetTargetHostName
 - sspi/SspiGetTargetHostName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - SspiCli.dll
api_name:
 - SspiGetTargetHostName
---

# SspiGetTargetHostName function


## -description

Gets the host name associated with the specified target.

## -parameters

### -param pszTargetName [in]

The target for which to get the host name.

### -param pszHostName [out]

The name of the host associated with the target specified by the <i>pszTargetName</i> parameter.

## -returns

If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.

