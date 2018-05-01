---
UID: NF:traceloggingprovider.TraceLoggingBinary
title: TraceLoggingBinary macro
author: windows-driver-content
description: Wrapper macro for raw binary data.
old-location: tracelogging\traceloggingbinary.htm
old-project: tracelogging
ms.assetid: A1CE1481-7319-41BE-9639-E688365D4628
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: TraceLoggingBinary, TraceLoggingBinary macro, tracelogging.traceloggingbinary, traceloggingprovider/TraceLoggingBinary
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
req.typenames: TPMVSCMGR_ERROR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	traceloggingprovider.h
api_name:
-	TraceLoggingBinary
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TraceLoggingBinary macro


## -description


Wrapper macro for raw binary data.


## -parameters




### -param pbData [in]

The binary data to process.


### -param cbData [in]

The size of the data in bytes.


#### - description [in, optional]

Description of the binary data. This parameter must be a literal string and will be included in the PDB. 


#### - name [in, optional]

The name of the data. This parameter must be a literal string and cannot contain any escape ('/0') characters. 


#### - tags [in, optional]

An integer value. The low 28 bits of the value will be included in the field's metadata and can be used by the event consumer for any purpose.

