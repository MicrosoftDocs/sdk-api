---
UID: NS:lpmapi.lpminitinfo
title: lpminitinfo
author: windows-sdk-content
description: The LPM_INIT_INFO structure contains local policy module initialization information.
old-location: qos\lpm_init_info.htm
old-project: QOS
ms.assetid: 7eab2cf0-97e6-4298-99c3-09ce8c09fb87
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: LPM_INIT_INFO, LPM_INIT_INFO structure [QOS], lpmapi/LPM_INIT_INFO, lpminitinfo, qos.lpm_init_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: LPM_INIT_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Lpmapi.h
api_name:
-	LPM_INIT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# lpminitinfo structure


## -description


The 
<b>LPM_INIT_INFO</b> structure contains local policy module initialization information.


## -struct-fields




### -field PcmVersionNumber

Version of the policy control module


### -field ResultTimeLimit

Time limit, in seconds, that the policy control module waits to receive results before timing out. 


### -field ConfiguredLpmCount

Number of configured local policy modules.


### -field AllocMemory

Memory allocation function used to initialize memory for local policy modules, in the form of a <a href="https://msdn.microsoft.com/e7b38820-4a7e-4f17-a67d-b94caa9037f5">PALLOCMEM</a> function.


### -field FreeMemory

Memory freeing function used to free memory allocated for the local policy module.  See <a href="https://msdn.microsoft.com/b700b5c1-9fd7-4fc9-a5ed-f8ac75d22037">PFREEMEM</a> for more information.


### -field PcmAdmitResultCallback

Callback function used to admit results. See <a href="https://msdn.microsoft.com/9040155b-6c6d-4deb-a63a-74e5fc8123ba">cbAdmitResult</a> for more information.


### -field GetRsvpObjectsCallback

Callback function used to obtain RSVP objects. See <a href="https://msdn.microsoft.com/baedb3e9-7768-4666-8bd7-78dd1d0eb0de">cbGetRsvpObjects</a> for more information.


## -see-also




<a href="https://msdn.microsoft.com/e7b38820-4a7e-4f17-a67d-b94caa9037f5">PALLOCMEM</a>



<a href="https://msdn.microsoft.com/b700b5c1-9fd7-4fc9-a5ed-f8ac75d22037">PFREEMEM</a>



<a href="https://msdn.microsoft.com/9040155b-6c6d-4deb-a63a-74e5fc8123ba">cbAdmitResult</a>



<a href="https://msdn.microsoft.com/baedb3e9-7768-4666-8bd7-78dd1d0eb0de">cbGetRsvpObjects</a>
 

 

