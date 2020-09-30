---
UID: NF:mi.MI_DestinationOptions_SetMaxEnvelopeSize
title: MI_DestinationOptions_SetMaxEnvelopeSize function (mi.h)
description: Sets the maximum packet size for transports.
helpviewer_keywords: ["MI_DestinationOptions_SetMaxEnvelopeSize","MI_DestinationOptions_SetMaxEnvelopeSize function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_SetMaxEnvelopeSize","wmi_v2.mi_destinationoptions_setmaxenvelopesize"]
old-location: wmi_v2\mi_destinationoptions_setmaxenvelopesize.htm
tech.root: wmi_v2
ms.assetid: 929a4a84-f23f-4d90-86c2-7ff4235a59c0
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_SetMaxEnvelopeSize, MI_DestinationOptions_SetMaxEnvelopeSize function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetMaxEnvelopeSize, wmi_v2.mi_destinationoptions_setmaxenvelopesize
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
 - MI_DestinationOptions_SetMaxEnvelopeSize
 - mi/MI_DestinationOptions_SetMaxEnvelopeSize
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
 - MI_DestinationOptions_SetMaxEnvelopeSize
---

# MI_DestinationOptions_SetMaxEnvelopeSize function


## -description

Sets the maximum packet size for transports.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a> function.

### -param sizeInKB

Maximum packet size.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.