---
UID: NE:tdh._DECODING_SOURCE
title: DECODING_SOURCE (tdh.h)
description: Defines the source of the event data.
helpviewer_keywords: ["DECODING_SOURCE","DECODING_SOURCE enumeration [ETW]","DecodingSourceTlg","DecodingSourceWPP","DecodingSourceWbem","DecodingSourceXMLFile","etw.decoding_source_enum","tdh.decoding_source_enum","tdh/DECODING_SOURCE","tdh/DecodingSourceTlg","tdh/DecodingSourceWPP","tdh/DecodingSourceWbem","tdh/DecodingSourceXMLFile"]
old-location: etw\decoding_source_enum.htm
tech.root: ETW
ms.assetid: d6cd09da-9a67-4df2-9d82-370c559d3bfc
ms.date: 12/05/2018
ms.keywords: DECODING_SOURCE, DECODING_SOURCE enumeration [ETW], DecodingSourceTlg, DecodingSourceWPP, DecodingSourceWbem, DecodingSourceXMLFile, etw.decoding_source_enum, tdh.decoding_source_enum, tdh/DECODING_SOURCE, tdh/DecodingSourceTlg, tdh/DecodingSourceWPP, tdh/DecodingSourceWbem, tdh/DecodingSourceXMLFile
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
req.typenames: DECODING_SOURCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DECODING_SOURCE
 - tdh/_DECODING_SOURCE
 - DECODING_SOURCE
 - tdh/DECODING_SOURCE
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
 - DECODING_SOURCE
---

# DECODING_SOURCE enumeration

## -description

Defines the source of the event data.

## -enum-fields

### -field DecodingSourceXMLFile

The source of the event data is a XML manifest.

### -field DecodingSourceWbem

The source of the event data is a WMI MOF class.

### -field DecodingSourceWPP

The source of the event data is a TMF file.

### -field DecodingSourceTlg

Indicates that the event was a self-describing event and was decoded using TraceLogging metadata.

### -field DecodingSourceMax

## -see-also
[TRACE_EVENT_INFO structure](ns-tdh-trace_event_info.md)
