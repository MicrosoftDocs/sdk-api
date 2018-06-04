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

# AMSI_RESULT enumeration


## -description


The <b>AMSI_RESULT</b> enumeration specifies the types of results returned by scans.


## -enum-fields




### -field AMSI_RESULT_CLEAN

Known good. No detection found, and the result is likely not going to change after a future definition update.


### -field AMSI_RESULT_NOT_DETECTED

No detection found, but the result might change after a future definition update.


### -field AMSI_RESULT_BLOCKED_BY_ADMIN_START

Administrator policy blocked this content on this machine (beginning of range).


### -field AMSI_RESULT_BLOCKED_BY_ADMIN_END

Administrator policy blocked this content on this machine (end of range).


### -field AMSI_RESULT_DETECTED

Detection found. The content is considered malware  and should be blocked.


## -remarks



The antimalware provider may return a result between 1 and 32767, inclusive, as an estimated risk level. The larger the result, the riskier it is to continue with the content. These values are provider specific, and may indicate a malware family or ID.

Results within the range of <b>AMSI_RESULT_BLOCKED_BY_ADMIN_START</b> and <b>AMSI_RESULT_BLOCKED_BY_ADMIN_END</b> values (inclusive) are officially blocked by the admin specified policy. In these cases, the script in question will be blocked from executing. The range is large to accommodate future additions in functionality.

Any return result equal to or larger than 32768 is considered malware,  and the content should be blocked. An app should use <a href="https://msdn.microsoft.com/1C7B48D9-FD1C-48B5-AA7F-0ED7382E106A">AmsiResultIsMalware</a> to determine if this is the case.



