---
UID: NF:winwlx.WlxGetConsoleSwitchCredentials
title: WlxGetConsoleSwitchCredentials function
author: windows-sdk-content
description: Winlogon calls this function to read the currently logged on user's credentials to transparently transfer them to a target session.
old-location: security\wlxgetconsoleswitchcredentials.htm
tech.root: SecAuthN
ms.assetid: ee6b3d03-11c9-4eb3-8c76-7041dddc755d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WlxGetConsoleSwitchCredentials, WlxGetConsoleSwitchCredentials function [Security], _gina_wlxgetconsoleswitchcredentials, security.wlxgetconsoleswitchcredentials, winwlx/WlxGetConsoleSwitchCredentials
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - Winwlx.h
api_name:
 - WlxGetConsoleSwitchCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WlxGetConsoleSwitchCredentials function


## -description


The <b>WlxGetConsoleSwitchCredentials</b> function must be implemented by a replacement <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> calls this function to read the currently logged on user's credentials to transparently transfer them to a target session.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param pWlxContext [in]

Pointer to a GINA-specific context.


### -param pCredInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/f72f3dd3-42a3-4f2b-be36-13c496c396fd">WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0</a> to return GINA relevant information.


## -returns



Returns <b>TRUE</b> on success and <b>FALSE</b> on failure.



