---
UID: NF:mi.MI_Deserializer_Close
title: MI_Deserializer_Close function (mi.h)
description: Closes a deserializer object and deletes any associated memory that is held within the deserializer.
helpviewer_keywords: ["MI_Deserializer_Close","MI_Deserializer_Close function [Windows Management Infrastructure (MI)]","mi/MI_Deserializer_Close","wmi_v2.mi_deserializer_close"]
old-location: wmi_v2\mi_deserializer_close.htm
tech.root: wmi_v2
ms.assetid: 34ddbd4f-723f-4580-aad6-c5c236a1f5d9
ms.date: 12/05/2018
ms.keywords: MI_Deserializer_Close, MI_Deserializer_Close function [Windows Management Infrastructure (MI)], mi/MI_Deserializer_Close, wmi_v2.mi_deserializer_close
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
 - MI_Deserializer_Close
 - mi/MI_Deserializer_Close
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
 - MI_Deserializer_Close
---

# MI_Deserializer_Close function


## -description

Closes a deserializer object and deletes any associated memory that is held within the deserializer.

## -parameters

### -param deserializer [in, out]

A pointer to the deserializer object to close.

## -returns

This function returns MI_INLINE MI_Result.

