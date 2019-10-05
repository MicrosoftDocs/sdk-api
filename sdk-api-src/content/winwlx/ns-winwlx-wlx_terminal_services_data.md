---
UID: NS:winwlx._WLX_TERMINAL_SERVICES_DATA
title: WLX_TERMINAL_SERVICES_DATA (winwlx.h)
author: windows-sdk-content
description: Used to provide GINA with Terminal Services user configuration information.
old-location: security\wlx_terminal_services_data.htm
tech.root: SecAuthN
ms.assetid: e3c6285e-cac3-490d-b2db-ea63871b3620
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PWLX_TERMINAL_SERVICES_DATA, PWLX_TERMINAL_SERVICES_DATA, PWLX_TERMINAL_SERVICES_DATA structure pointer [Security], WLX_TERMINAL_SERVICES_DATA, WLX_TERMINAL_SERVICES_DATA structure [Security], _gina_wlx_terminal_services_data, security.wlx_terminal_services_data, winwlx/PWLX_TERMINAL_SERVICES_DATA, winwlx/WLX_TERMINAL_SERVICES_DATA"
ms.topic: struct
f1_keywords: 
 - "winwlx/WLX_TERMINAL_SERVICES_DATA"
dev_langs:
 - c++
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
 - HeaderDef
api_location:
 - Winwlx.h
api_name:
 - WLX_TERMINAL_SERVICES_DATA
targetos: Windows
req.typenames: WLX_TERMINAL_SERVICES_DATA, *PWLX_TERMINAL_SERVICES_DATA
req.redist: 
ms.custom: 19H1
---

# WLX_TERMINAL_SERVICES_DATA structure


## -description


<p class="CCE_Message">[The WLX_TERMINAL_SERVICES_DATA structure is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WLX_TERMINAL_SERVICES_DATA</b> structure is used to provide <a href="https://docs.microsoft.com/windows/desktop/SecGloss/g-gly">GINA</a> with Terminal Services user configuration information.

The structure is populated by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data">WlxQueryTerminalServicesData</a> function.


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




<a href="https://docs.microsoft.com/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data">WlxQueryTerminalServicesData</a>
 

 

