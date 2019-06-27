---
UID: NE:wbemcli.tag_WBEM_REFRESHER_FLAGS
title: WBEM_REFRESHER_FLAGS (wbemcli.h)
author: windows-sdk-content
description: Contains flags that modify the behavior of refresher methods.
old-location: wmi\wbem_refresher_flags.htm
tech.root: WmiSdk
ms.assetid: F855478C-BF26-46B1-B3F8-9DD5E8F05862
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WBEM_FLAG_REFRESH_AUTO_RECONNECT, WBEM_FLAG_REFRESH_NO_AUTO_RECONNECT, WBEM_REFRESHER_FLAGS, WBEM_REFRESHER_FLAGS enumeration [Windows Management Instrumentation], wbemcli/WBEM_FLAG_REFRESH_AUTO_RECONNECT, wbemcli/WBEM_FLAG_REFRESH_NO_AUTO_RECONNECT, wbemcli/WBEM_REFRESHER_FLAGS, wmi.wbem_refresher_flags
ms.topic: enum
f1_keywords: 
 - "wbemcli/WBEM_REFRESHER_FLAGS"
req.header: wbemcli.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - Wbemcli.h
api_name:
 - WBEM_REFRESHER_FLAGS
product: Windows
targetos: Windows
req.typenames: WBEM_REFRESHER_FLAGS
req.redist: 
ms.custom: 19H1
---

# WBEM_REFRESHER_FLAGS enumeration


## -description


Contains flags that modify the behavior of refresher methods.


## -enum-fields




### -field WBEM_FLAG_REFRESH_AUTO_RECONNECT

If the connection is broken, the refresher attempts to reconnect to the provider automatically.


### -field WBEM_FLAG_REFRESH_NO_AUTO_RECONNECT

If the connection is broken, the refresher does not attempt to reconnect to the provider automatically.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-remove">IWbemConfigureRefresher::Remove</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemrefresher-refresh">IWbemRefresher::Refresh</a>
 

 

