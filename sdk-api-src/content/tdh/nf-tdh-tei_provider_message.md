---
UID: NF:tdh.TEI_PROVIDER_MESSAGE
tech.root: ETW
title: TEI_PROVIDER_MESSAGE (tdh.h)
ms.date: 12/05/2022
ms.keywords: TEI_PROVIDER_MESSAGE
targetos: Windows
description: Macro that retrieves the Trace Event Information (TEI) provider message.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: tdh.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - tdh.h
api_name:
 - TEI_PROVIDER_MESSAGE
f1_keywords:
 - TEI_PROVIDER_MESSAGE
 - tdh/TEI_PROVIDER_MESSAGE
dev_langs:
 - c++
helpviewer_keywords:
 - TEI_PROVIDER_MESSAGE
---

# TEI_PROVIDER_MESSAGE function (tdh.h)

## -description

Macro that retrieves the Trace Event Information (TEI) provider message.

## -parameters

### -param EventInfo [in]

A [TRACE_EVENT_INFO structure](ns-tdh-trace_event_info.md) that contains the event information. To get this structure, call the [TdhGetEventInformation function](nf-tdh-tdhgeteventinformation.md).

## -returns

The TEI provider message, or NULL.

## -remarks

## -see-also
