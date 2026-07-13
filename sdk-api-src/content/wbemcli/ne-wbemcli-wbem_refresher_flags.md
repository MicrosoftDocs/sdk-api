---
UID: NE:wbemcli.tag_WBEM_REFRESHER_FLAGS
title: WBEM_REFRESHER_FLAGS (wbemcli.h)
description: Contains flags that modify the behavior of refresher methods.
helpviewer_keywords: ["WBEM_FLAG_REFRESH_AUTO_RECONNECT","WBEM_FLAG_REFRESH_NO_AUTO_RECONNECT","WBEM_REFRESHER_FLAGS","WBEM_REFRESHER_FLAGS enumeration [Windows Management Instrumentation]","wbemcli/WBEM_FLAG_REFRESH_AUTO_RECONNECT","wbemcli/WBEM_FLAG_REFRESH_NO_AUTO_RECONNECT","wbemcli/WBEM_REFRESHER_FLAGS","wmi.wbem_refresher_flags"]
old-location: wmi\wbem_refresher_flags.htm
tech.root: wmi
ms.assetid: F855478C-BF26-46B1-B3F8-9DD5E8F05862
ms.date: 12/05/2018
ms.keywords: WBEM_FLAG_REFRESH_AUTO_RECONNECT, WBEM_FLAG_REFRESH_NO_AUTO_RECONNECT, WBEM_REFRESHER_FLAGS, WBEM_REFRESHER_FLAGS enumeration [Windows Management Instrumentation], wbemcli/WBEM_FLAG_REFRESH_AUTO_RECONNECT, wbemcli/WBEM_FLAG_REFRESH_NO_AUTO_RECONNECT, wbemcli/WBEM_REFRESHER_FLAGS, wmi.wbem_refresher_flags
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
targetos: Windows
req.typenames: WBEM_REFRESHER_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_WBEM_REFRESHER_FLAGS
 - wbemcli/tag_WBEM_REFRESHER_FLAGS
 - WBEM_REFRESHER_FLAGS
 - wbemcli/WBEM_REFRESHER_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemcli.h
api_name:
 - WBEM_REFRESHER_FLAGS
---

# WBEM_REFRESHER_FLAGS enumeration


## -description

Contains flags that modify the behavior of refresher methods.

## -enum-fields

### -field WBEM_FLAG_REFRESH_AUTO_RECONNECT:0

If the connection is broken, the refresher attempts to reconnect to the provider automatically.

### -field WBEM_FLAG_REFRESH_NO_AUTO_RECONNECT:1

If the connection is broken, the refresher does not attempt to reconnect to the provider automatically.

## -see-also

<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-remove">IWbemConfigureRefresher::Remove</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemrefresher-refresh">IWbemRefresher::Refresh</a>
