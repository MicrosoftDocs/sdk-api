---
UID: NF:traceloggingprovider.TraceLoggingCustom
title: TraceLoggingCustom macro (traceloggingprovider.h)
description: Wrapper macro for an event field packed using a custom serializer.
helpviewer_keywords: ["TraceLoggingCustom","TraceLoggingCustom macro","tracelogging.traceloggingcustom","traceloggingprovider/TraceLoggingCustom"]
old-location: tracelogging\traceloggingcustom.htm
tech.root: tracelogging
ms.assetid: 617B5EFF-DB4F-493E-841B-14BBA312E26B
ms.date: 12/05/2018
ms.keywords: TraceLoggingCustom, TraceLoggingCustom macro, tracelogging.traceloggingcustom, traceloggingprovider/TraceLoggingCustom
req.header: traceloggingprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2012 R2
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TraceLoggingCustom
 - traceloggingprovider/TraceLoggingCustom
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - traceloggingprovider.h
api_name:
 - TraceLoggingCustom
---

# TraceLoggingCustom macro


## -description

Wrapper macro for an event field packed using a custom serializer.

Provides the possibility to write a custom serializer and deserializer for data and have TraceLogging handle packing and unpacking metadata for the field.

## -parameters

### -param pbValue [in]

The field payload serialized at runtime
by a serializer from the specified protocol family.

### -param cbValue [in]

The size in bytes of the  field payload serialized at runtime
by a serializer from the specified protocol family.

### -param protocol [in]

A protocol family, which may be specified Microsoft-defined value from 0-4 or a user-defined value from 5-31. (The Microsoft-defined values are defined by macros starting with TRACELOGGING_PROTOCOL_.)

### -param bSchema [in]

A comma-separated list of byte values that contain the information needed to decode the payload (i.e. the schema), in a protocol-defined format. The values in this list must be compile-time constant. Example: (0x12, 0x23, 0x34)

### -param cbSchema [in]

The number of byte values provided in <b>bSchema</b>. This value must be a compile-time constant.


#### - description [in, optional]

The description of the event field's value. If provided, the description parameter must be a string literal, and will be included in the PDB. 


#### - name [in, optional]

The name of the event field. If provided, the name parameter must be a string literal (not a variable) and must not  contain any '\0' characters.


#### - tags [in, optional]

An integer value. The low 28 bits of the value will be included in the field's metadata. The semantics of the tags  are defined by the event consumer. During event processing, this tag can be retrieved from the EVENT_PROPERTY_INFO Tags field.

## -remarks

Decoders should access TraceLoggingCustom serialized fields using the TDH APIs. The TRACE_EVENT_INFO structure returned by TdhGetEventInformation will contain two EVENT_PROPERTY_INFO structures related to a logged TraceLoggingCustom field. These correlate in the typical fashion with the data found in the EVENT_RECORD’s UserData blob.



The first of the two EVENT_PROPERTY_INFO structures is the “Length” property which describes the length of the serialized payload (i.e. cbValue). 

The second is the property that refers to the user's payload (pbValue). The second property will have PropertyParamLength (in reference to the first of the two properties) and PropertyHasCustomSchema set.



Decoders should recognize PropertyHasCustomSchema has been set and consult this EVENT_PROPERTY_INFO’s customSchemaType member for the CustomSchemaOffset, the offset in the TRACE_EVENT_INFORMATION where the protocol type and protocol metadata are located. There, they can find the metadata they passed in with a format of (pseudo-struct):


<pre class="syntax">struct _CUSTOM_SCHEMA {
    UINT16 protocolType;
    UINT16 cbSchema;
    BYTE bSchema[cbSchema];
}</pre>


Existing decoders that do not take these extra steps to recognize the PropertyHasCustomSchema flag and instead refer to the nonStructType part of the EVENT_PROPERTY_INFO union to decode the event will seamlessly treat the payload as if it were TDH_INTYPE_BINARY.


#### Examples


```cpp
BYTE rgValue[] = {...};

TraceLoggingWrite(
   g_hProvider,
   "MyEventName",
   TraceLoggingCustom(
      rgValue, 
      sizeof(rgValue), 
      TRACELOGGING_PROTOCOL_MYPROTOCOL,
      ( 0x0, 0x1, 0x2 ),
      3,
      "MyCustomField"
   ));
```

