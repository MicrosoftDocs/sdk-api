---
UID: NS:objidl.tagRemSNB
title: RemSNB
author: windows-sdk-content
description: The RemSNB structure is used for marshaling the SNB data type.Defined in the IStorage interface (Storag.idl).
old-location: stg\remsnb.htm
tech.root: stg
ms.assetid: 09a50518-2889-49ca-9d81-3035777ac2ac
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*wireSNB, RemSNB, RemSNB structure [Structured Storage], SNB, SNB structure pointer [Structured Storage], _stg_remsnb, objidl/RemSNB, objidl/SNB, stg.remsnb"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objidl.h
api_name:
 - RemSNB
product: Windows
targetos: Windows
req.typenames: RemSNB
req.redist: 
---

# RemSNB structure


## -description


The 
<b>RemSNB</b> structure is used for marshaling the 
<a href="https://msdn.microsoft.com/8428a820-3d8a-41e0-9955-d355440e2ebc">SNB</a> data type.

Defined in the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface (Storag.idl).


## -struct-fields




### -field ulCntStr

Number of strings in the <b>rgString</b> buffer.


### -field ulCntChar

Size in bytes of the <b>rgString</b> buffer.


### -field rgString

Pointer to an array of bytes containing the stream name strings from the <b>SNB</b> structure.


## -see-also




<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>
 

 

