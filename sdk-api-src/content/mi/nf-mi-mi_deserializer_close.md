---
UID: NF:mi.MI_Deserializer_Close
title: MI_Deserializer_Close function
author: windows-driver-content
description: Closes a deserializer object and deletes any associated memory that is held within the deserializer.
old-location: wmi_v2\mi_deserializer_close.htm
old-project: wmi_v2
ms.assetid: 34ddbd4f-723f-4580-aad6-c5c236a1f5d9
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: MI_Deserializer_Close, MI_Deserializer_Close function [Windows Management Infrastructure (MI)], mi/MI_Deserializer_Close, wmi_v2.mi_deserializer_close
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_Deserializer_Close
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Deserializer_Close function


## -description


Closes a deserializer object and deletes any associated memory that is held within the deserializer.


## -parameters




### -param deserializer [in, out]

A pointer to the deserializer object to close.


## -returns



This function returns MI_INLINE MI_Result.



