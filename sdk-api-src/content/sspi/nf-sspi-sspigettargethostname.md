---
UID: NF:sspi.SspiGetTargetHostName
title: SspiGetTargetHostName function
author: windows-sdk-content
description: Gets the host name associated with the specified target.
old-location: security\sspigettargethostname.htm
old-project: secauthn
ms.assetid: 84570dfc-1890-4b82-b411-1f9eaa75537b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SspiGetTargetHostName, SspiGetTargetHostName function [Security], security.sspigettargethostname, sspi/SspiGetTargetHostName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS, *PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - SspiCli.dll
api_name:
 - SspiGetTargetHostName
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: SspiCli.dll
req.irql: 
req.product: Outlook Express 6.0
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



