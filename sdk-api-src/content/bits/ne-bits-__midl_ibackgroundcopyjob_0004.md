---
UID: NE:bits.__MIDL_IBackgroundCopyJob_0004
title: "__MIDL_IBackgroundCopyJob_0004"
author: windows-driver-content
description: The BG_JOB_PROXY_USAGE enumeration defines constant values that specify which proxy to use for file transfers. You can define different proxy settings for each job.
old-location: bits\bg_job_proxy_usage.htm
old-project: Bits
ms.assetid: e066b6c8-905f-4e18-9be7-aa3c134f9e13
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: BG_JOB_PROXY_USAGE, BG_JOB_PROXY_USAGE enumeration [BITS], BG_JOB_PROXY_USAGE_AUTODETECT, BG_JOB_PROXY_USAGE_NO_PROXY, BG_JOB_PROXY_USAGE_OVERRIDE, BG_JOB_PROXY_USAGE_PRECONFIG, __MIDL_IBackgroundCopyJob_0004, _drz_bg_job_proxy_usage, bits.bg_job_proxy_usage, bits/BG_JOB_PROXY_USAGE, bits/BG_JOB_PROXY_USAGE_AUTODETECT, bits/BG_JOB_PROXY_USAGE_NO_PROXY, bits/BG_JOB_PROXY_USAGE_OVERRIDE, bits/BG_JOB_PROXY_USAGE_PRECONFIG
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Bits.h
api_name:
-	BG_JOB_PROXY_USAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

