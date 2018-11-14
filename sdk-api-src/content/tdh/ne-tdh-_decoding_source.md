---
UID: NE:tdh._DECODING_SOURCE
title: "_DECODING_SOURCE"
author: windows-sdk-content
description: Defines the source of the event data.
old-location: etw\decoding_source_enum.htm
tech.root: etw
ms.assetid: d6cd09da-9a67-4df2-9d82-370c559d3bfc
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DECODING_SOURCE, DECODING_SOURCE enumeration [ETW], DecodingSourceTlg, DecodingSourceWPP, DecodingSourceWbem, DecodingSourceXMLFile, _DECODING_SOURCE, etw.decoding_source_enum, tdh.decoding_source_enum, tdh/DECODING_SOURCE, tdh/DecodingSourceTlg, tdh/DecodingSourceWPP, tdh/DecodingSourceWbem, tdh/DecodingSourceXMLFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tdh.h
api_name:
 - DECODING_SOURCE
product: Windows
targetos: Windows
req.typenames: DECODING_SOURCE
req.redist: 
---

# _DECODING_SOURCE enumeration


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




<a href="https://msdn.microsoft.com/ecf57a23-0dd2-4954-82ac-e92f651c226f">TRACE_EVENT_INFO</a>
 

 

