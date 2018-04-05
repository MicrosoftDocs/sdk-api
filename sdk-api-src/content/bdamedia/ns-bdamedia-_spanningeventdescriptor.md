---
UID: NS:bdamedia._SpanningEventDescriptor
title: "_SpanningEventDescriptor"
author: windows-driver-content
description: Contains information about an MPEG-2 descriptor.
old-location: mstv\spanningeventdescriptor.htm
old-project: mstv
ms.assetid: d394b0c9-a61a-44e8-972d-0c12fd446e59
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: SpanningEventDescriptor, SpanningEventDescriptor structure [Microsoft TV Technologies], _SpanningEventDescriptor, bdamedia/SpanningEventDescriptor, mstv.spanningeventdescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bdamedia.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SpanningEventDescriptor
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	bdamedia.h
api_name:
-	SpanningEventDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _SpanningEventDescriptor structure


## -description


Contains information about an MPEG-2 descriptor.


## -struct-fields




### -field wDataLen

Total size of the structure in bytes, including the size of the <b>bDescriptor</b> array.


### -field wProgNumber

The program number associated with the descriptor.


### -field wSID

The service ID associted with the descriptor.


### -field bDescriptor

A byte array with the following layout:

<ul>
<li>Byte 0 contains the descriptor tag.</li>
<li>Byte 1 contains the length of the descriptor body.</li>
<li>The remaining bytes contain the descriptor body.</li>
</ul>
The array is larger than the size given in the structure declaration. Use the value of <b>wDataLen</b> to determine the size.

