---
UID: NS:rtmv2._RTM_ENTITY_EXPORT_METHODS
title: RTM_ENTITY_EXPORT_METHODS (rtmv2.h)
description: The RTM_ENTITY_EXPORT_METHODS structure contains the set of methods exported by a client.
helpviewer_keywords: ["*PRTM_ENTITY_EXPORT_METHODS","PRTM_ENTITY_EXPORT_METHODS","PRTM_ENTITY_EXPORT_METHODS structure pointer [RAS]","RTM_ENTITY_EXPORT_METHODS","RTM_ENTITY_EXPORT_METHODS structure [RAS]","_rtmv2ref_rtm_entity_export_methods","rras.rtm_entity_export_methods","rtmv2/PRTM_ENTITY_EXPORT_METHODS","rtmv2/RTM_ENTITY_EXPORT_METHODS"]
old-location: rras\rtm_entity_export_methods.htm
tech.root: RRAS
ms.assetid: 8198cfad-9188-4f49-92ab-1750ec16aec4
ms.date: 12/05/2018
ms.keywords: '*PRTM_ENTITY_EXPORT_METHODS, PRTM_ENTITY_EXPORT_METHODS, PRTM_ENTITY_EXPORT_METHODS structure pointer [RAS], RTM_ENTITY_EXPORT_METHODS, RTM_ENTITY_EXPORT_METHODS structure [RAS], _rtmv2ref_rtm_entity_export_methods, rras.rtm_entity_export_methods, rtmv2/PRTM_ENTITY_EXPORT_METHODS, rtmv2/RTM_ENTITY_EXPORT_METHODS'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RTM_ENTITY_EXPORT_METHODS, *PRTM_ENTITY_EXPORT_METHODS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RTM_ENTITY_EXPORT_METHODS
 - rtmv2/_RTM_ENTITY_EXPORT_METHODS
 - PRTM_ENTITY_EXPORT_METHODS
 - rtmv2/PRTM_ENTITY_EXPORT_METHODS
 - RTM_ENTITY_EXPORT_METHODS
 - rtmv2/RTM_ENTITY_EXPORT_METHODS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rtmv2.h
api_name:
 - RTM_ENTITY_EXPORT_METHODS
---

# RTM_ENTITY_EXPORT_METHODS structure


## -description

The 
<b>RTM_ENTITY_EXPORT_METHODS</b> structure contains the set of methods exported by a client.

## -struct-fields

### -field NumMethods

Specifies the number of methods exported by the client in the <b>Methods</b> member.

### -field Methods

Specifies which methods the client is exporting.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>