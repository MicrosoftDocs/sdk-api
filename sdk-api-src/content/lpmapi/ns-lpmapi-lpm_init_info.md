---
UID: NS:lpmapi.lpminitinfo
title: LPM_INIT_INFO (lpmapi.h)
description: The LPM_INIT_INFO structure contains local policy module initialization information.
helpviewer_keywords: ["LPM_INIT_INFO","LPM_INIT_INFO structure [QOS]","lpmapi/LPM_INIT_INFO","qos.lpm_init_info"]
old-location: qos\lpm_init_info.htm
tech.root: QOS
ms.assetid: 7eab2cf0-97e6-4298-99c3-09ce8c09fb87
ms.date: 12/05/2018
ms.keywords: LPM_INIT_INFO, LPM_INIT_INFO structure [QOS], lpmapi/LPM_INIT_INFO, qos.lpm_init_info
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LPM_INIT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lpminitinfo
 - lpmapi/lpminitinfo
 - LPM_INIT_INFO
 - lpmapi/LPM_INIT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - LPM_INIT_INFO
---

# LPM_INIT_INFO structure


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

Memory allocation function used to initialize memory for local policy modules, in the form of a <a href="/previous-versions/windows/desktop/api/lpmapi/nc-lpmapi-pallocmem">PALLOCMEM</a> function.

### -field FreeMemory

Memory freeing function used to free memory allocated for the local policy module.  See <a href="/previous-versions/windows/desktop/api/lpmapi/nc-lpmapi-pfreemem">PFREEMEM</a> for more information.

### -field PcmAdmitResultCallback

Callback function used to admit results. See <a href="/previous-versions/windows/desktop/api/lpmapi/nc-lpmapi-cbadmitresult">cbAdmitResult</a> for more information.

### -field GetRsvpObjectsCallback

Callback function used to obtain RSVP objects. See <a href="/previous-versions/windows/desktop/api/lpmapi/nc-lpmapi-cbgetrsvpobjects">cbGetRsvpObjects</a> for more information.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/nc-lpmapi-pallocmem">PALLOCMEM</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/nc-lpmapi-pfreemem">PFREEMEM</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/nc-lpmapi-cbadmitresult">cbAdmitResult</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/nc-lpmapi-cbgetrsvpobjects">cbGetRsvpObjects</a>