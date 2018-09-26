---
UID: NC:winwlx.PWLX_QUERY_CONSOLESWITCH_CREDENTIALS
title: PWLX_QUERY_CONSOLESWITCH_CREDENTIALS
author: windows-sdk-content
description: Called by GINA to read the credentials transferred from the Winlogon of the temporary session to the Winlogon of the destination session.
old-location: security\wlxqueryconsoleswitchcredentials.htm
tech.root: secauthn
ms.assetid: cbb9342e-c06a-4040-9c6c-c761195734a4
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: PWLX_QUERY_CONSOLESWITCH_CREDENTIALS, PWLX_QUERY_CONSOLESWITCH_CREDENTIALS callback, WlxQueryConsoleSwitchCredentials, WlxQueryConsoleSwitchCredentials callback function [Security], _gina_wlxqueryconsoleswitchcredentials, security.wlxqueryconsoleswitchcredentials, winwlx/WlxQueryConsoleSwitchCredentials
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winwlx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - winwlx.h
api_name:
 - WlxQueryConsoleSwitchCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWLX_QUERY_CONSOLESWITCH_CREDENTIALS callback function


## -description


Called by <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> to read the credentials transferred from the Winlogon of the temporary session to the Winlogon of the destination session.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param pCred [out]

Pointer to a 
<a href="https://msdn.microsoft.com/f72f3dd3-42a3-4f2b-be36-13c496c396fd">WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0</a> structure to be filled with credentials information.


## -returns



Returns <b>TRUE</b> if credentials were transferred and <b>FALSE</b> if the transfer failed.




## -remarks



In order to access this function, the GINA DLL must use the 
<a href="https://msdn.microsoft.com/b2d0c936-5430-48ed-b808-92209b909406">WLX_DISPATCH_VERSION_1_4</a> structure.



