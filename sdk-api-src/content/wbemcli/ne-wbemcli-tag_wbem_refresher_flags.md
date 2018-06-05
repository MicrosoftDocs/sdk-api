---
UID: NE:wbemcli.tag_WBEM_REFRESHER_FLAGS
title: tag_WBEM_REFRESHER_FLAGS
author: windows-sdk-content
description: Contains flags that modify the behavior of refresher methods.
old-location: wmi\wbem_refresher_flags.htm
old-project: WmiSdk
ms.assetid: F855478C-BF26-46B1-B3F8-9DD5E8F05862
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: WBEM_FLAG_REFRESH_AUTO_RECONNECT, WBEM_FLAG_REFRESH_NO_AUTO_RECONNECT, WBEM_REFRESHER_FLAGS, WBEM_REFRESHER_FLAGS enumeration [Windows Management Instrumentation], tag_WBEM_REFRESHER_FLAGS, wbemcli/WBEM_FLAG_REFRESH_AUTO_RECONNECT, wbemcli/WBEM_FLAG_REFRESH_NO_AUTO_RECONNECT, wbemcli/WBEM_REFRESHER_FLAGS, wmi.wbem_refresher_flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: WBEM_REFRESHER_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wbemcli.h
api_name:
-	WBEM_REFRESHER_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tag_WBEM_REFRESHER_FLAGS enumeration


## -description


Contains flags that modify the behavior of refresher methods.


## -enum-fields




### -field WBEM_FLAG_REFRESH_AUTO_RECONNECT

If the connection is broken, the refresher attempts to reconnect to the provider automatically.


### -field WBEM_FLAG_REFRESH_NO_AUTO_RECONNECT

If the connection is broken, the refresher does not attempt to reconnect to the provider automatically.


## -see-also




<a href="https://msdn.microsoft.com/f6e68b95-e9d1-473e-add4-823b6db51709">IWbemConfigureRefresher::Remove</a>



<a href="https://msdn.microsoft.com/6de85040-c938-41dc-8240-0e21e89c7716">IWbemRefresher::Refresh</a>
 

 

