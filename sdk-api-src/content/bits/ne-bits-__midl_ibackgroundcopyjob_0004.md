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

# __MIDL_IBackgroundCopyJob_0004 enumeration


## -description


The 
<b>BG_JOB_PROXY_USAGE</b> enumeration defines constant values that specify which proxy to use for file transfers. You can define different proxy settings for each job.


## -enum-fields




### -field BG_JOB_PROXY_USAGE_PRECONFIG

Use the proxy and proxy bypass list settings defined by each user to transfer files. Settings are user-defined from Control Panel, Internet Options, Connections, Local Area Network (LAN) settings (or Dial-up settings, depending on the network connection).


### -field BG_JOB_PROXY_USAGE_NO_PROXY

Do not use a proxy to transfer files. Use this option when you transfer files within a LAN.


### -field BG_JOB_PROXY_USAGE_OVERRIDE

Use the application's proxy and proxy bypass list to transfer files. Use this option when you cannot trust that the system settings are correct. Also use this option when you want to transfer files using a special account, such as LocalSystem, to which the system settings do not apply.


### -field BG_JOB_PROXY_USAGE_AUTODETECT

Automatically detect proxy settings. BITS detects proxy settings for each file in the job.

<b>BITS 1.5 and earlier:  </b><b>BG_JOB_PROXY_USAGE_AUTODETECT</b> is not available.


## -see-also




<a href="https://msdn.microsoft.com/c2d0ec9b-eaa1-4f78-9ccc-4e91d045cd94">IBackgroundCopyJob::GetProxySettings</a>



<a href="https://msdn.microsoft.com/fd21a17b-1049-4dd9-a08b-da84699b8006">IBackgroundCopyJob::SetProxySettings</a>
 

 

