---
UID: NS:tdh._TDH_CONTEXT
title: TDH_CONTEXT (tdh.h)
description: Defines the additional information required to parse an event.
helpviewer_keywords: ["*PTDH_CONTEXT","TDH_CONTEXT","TDH_CONTEXT structure [ETW]","etw.tdh_context_struct","tdh.tdh_context_struct","tdh/TDH_CONTEXT"]
old-location: etw\tdh_context_struct.htm
tech.root: ETW
ms.assetid: 184df0af-3ac5-406f-a298-4f23826ad85e
ms.date: 12/05/2018
ms.keywords: '*PTDH_CONTEXT, TDH_CONTEXT, TDH_CONTEXT structure [ETW], etw.tdh_context_struct, tdh.tdh_context_struct, tdh/TDH_CONTEXT'
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: TDH_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TDH_CONTEXT
 - tdh/_TDH_CONTEXT
 - TDH_CONTEXT
 - tdh/TDH_CONTEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tdh.h
api_name:
 - TDH_CONTEXT
---

# TDH_CONTEXT structure


## -description

Defines the additional information required to parse an event.

## -struct-fields

### -field ParameterValue

Context value cast to a ULONGLONG. The context value is determined by the context type specified in <b>ParameterType</b>. For example, if the context type is TDH_CONTEXT_WPP_TMFFILE, the context value is a Unicode string that contains the name of the .tmf file.

### -field ParameterType

Context type. For a list of types, see the <a href="/windows/desktop/api/tdh/ne-tdh-tdh_context_type">TDH_CONTEXT_TYPE</a> enumeration.

### -field ParameterSize

Reserved for future use.

## -see-also
<a href="/windows/desktop/api/tdh/nf-tdh-tdhgeteventinformation">TdhGetEventInformation</a>