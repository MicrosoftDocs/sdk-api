---
UID: NS:winwlx._WLX_TERMINAL_SERVICES_DATA
title: "_WLX_TERMINAL_SERVICES_DATA"
author: windows-sdk-content
description: Used to provide GINA with Terminal Services user configuration information.
old-location: security\wlx_terminal_services_data.htm
old-project: SecAuthN
ms.assetid: e3c6285e-cac3-490d-b2db-ea63871b3620
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: "*PWLX_TERMINAL_SERVICES_DATA, PWLX_TERMINAL_SERVICES_DATA, PWLX_TERMINAL_SERVICES_DATA structure pointer [Security], WLX_TERMINAL_SERVICES_DATA, WLX_TERMINAL_SERVICES_DATA structure [Security], _WLX_TERMINAL_SERVICES_DATA, _gina_wlx_terminal_services_data, security.wlx_terminal_services_data, winwlx/PWLX_TERMINAL_SERVICES_DATA, winwlx/WLX_TERMINAL_SERVICES_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WLX_TERMINAL_SERVICES_DATA, *PWLX_TERMINAL_SERVICES_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winwlx.h
api_name:
 - WLX_TERMINAL_SERVICES_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WLX_TERMINAL_SERVICES_DATA structure


## -description


<p class="CCE_Message">[The WLX_TERMINAL_SERVICES_DATA structure is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WLX_TERMINAL_SERVICES_DATA</b> structure is used to provide <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> with Terminal Services user configuration information.

The structure is populated by the 
<a href="https://msdn.microsoft.com/a7b81d76-74de-44a8-92ad-765ad1f7013e">WlxQueryTerminalServicesData</a> function.


## -struct-fields




### -field ProfilePath

Terminal Services profile path, overrides the standard profile path.


### -field HomeDir

Terminal Services home directory, overrides standard home directory.


### -field HomeDirDrive

Terminal Services home directory drive, overrides the standard drive.


## -remarks



The Terminal Services user configuration information is received from the Domain Controller and SAM database.




## -see-also




<a href="https://msdn.microsoft.com/a7b81d76-74de-44a8-92ad-765ad1f7013e">WlxQueryTerminalServicesData</a>
 

 

