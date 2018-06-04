---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WlxGetConsoleSwitchCredentials function


## -description



			The <b>WlxGetConsoleSwitchCredentials</b> function must be implemented by a replacement <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a> calls this function to read the currently logged on user's credentials to transparently transfer them to a target session.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param pWlxContext [in]

Pointer to a GINA-specific context.


### -param pCredInfo

TBD




#### - pInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/f72f3dd3-42a3-4f2b-be36-13c496c396fd">WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0</a> to return GINA relevant information.


## -returns




						Returns <b>TRUE</b> on success and <b>FALSE</b> on failure.



