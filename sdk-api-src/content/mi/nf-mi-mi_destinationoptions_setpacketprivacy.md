---
UID: NF:mi.MI_DestinationOptions_SetPacketPrivacy
title: MI_DestinationOptions_SetPacketPrivacy function (mi.h)
description: Enables or disables packet privacy (encryption).
helpviewer_keywords: ["MI_DestinationOptions_SetPacketPrivacy","MI_DestinationOptions_SetPacketPrivacy function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_SetPacketPrivacy","wmi_v2.mi_destinationoptions_setpacketprivacy"]
old-location: wmi_v2\mi_destinationoptions_setpacketprivacy.htm
tech.root: wmi_v2
ms.assetid: bb047646-fa95-4691-946c-5faf5b7edc8b
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_SetPacketPrivacy, MI_DestinationOptions_SetPacketPrivacy function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetPacketPrivacy, wmi_v2.mi_destinationoptions_setpacketprivacy
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_DestinationOptions_SetPacketPrivacy
 - mi/MI_DestinationOptions_SetPacketPrivacy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_DestinationOptions_SetPacketPrivacy
---

# MI_DestinationOptions_SetPacketPrivacy function


## -description

Enables or disables packet privacy (encryption).

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a> function.

### -param privacy

Boolean value where <b>MI_TRUE</b> means to use encryption and <b>MI_FALSE</b> means to not use encryption.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

The default value for this setting is <b>MI_TRUE</b>.