---
UID: NS:rtmv2._RTM_PREF_INFO
title: "_RTM_PREF_INFO"
author: windows-sdk-content
description: The RTM_PREF_INFO structure contains the information used when comparing any two routes. The value of the Preference member is given more weight than the value of the Metric member.
old-location: rras\rtm_pref_info.htm
old-project: RRAS
ms.assetid: 50aa7f8e-9d89-44bd-897e-f0040f579d24
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: "*PRTM_PREF_INFO, PRTM_PREF_INFO, PRTM_PREF_INFO structure pointer [RAS], RTM_PREF_INFO, RTM_PREF_INFO structure [RAS], _RTM_PREF_INFO, _rtmv2ref_rtm_pref_info, rras.rtm_pref_info, rtmv2/PRTM_PREF_INFO, rtmv2/RTM_PREF_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: rtmv2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: RTM_PREF_INFO, *PRTM_PREF_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Rtmv2.h
api_name:
-	RTM_PREF_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _RTM_PREF_INFO structure


## -description


The 
<b>RTM_PREF_INFO</b> structure contains the information used when comparing any two routes. The value of the <b>Preference</b> member is given more weight than the value of the <b>Metric</b> member.


## -struct-fields




### -field Metric

Specifies a metric. The metric is specific to a particular routing protocol.


### -field Preference

Specifies a preference. The preference is determined by the router policy.


## -remarks



Preference is more important than metric. The metric is only  checked if the preferences are equal.




## -see-also




<a href="https://msdn.microsoft.com/7d9bf8c0-dc09-440a-b60d-97463c70a745">RTM_ROUTE_INFO</a>
 

 

