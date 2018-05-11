---
UID: NF:mi.MI_Serializer_Close
title: MI_Serializer_Close function
author: windows-driver-content
description: Closes a serializer object and frees any internal memory associated with it.
old-location: wmi_v2\mi_serializer_close.htm
old-project: wmi_v2
ms.assetid: fbae767d-1f30-4b73-8978-ea14ce707303
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: MI_Serializer_Close, MI_Serializer_Close function [Windows Management Infrastructure (MI)], mi/MI_Serializer_Close, wmi_v2.mi_serializer_close
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
-	MI_Serializer_Close
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Serializer_Close function


## -description


Closes a serializer object and frees any internal memory associated with it.


## -parameters




### -param serializer [in, out]

A pointer to a serializer returned from the <a href="https://msdn.microsoft.com/9de29d43-0677-4dc9-927f-af7c01179991">MI_Application_NewSerializer</a> function.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



This function should be called if there are no more active calls into the serializer.




## -see-also




<a href="https://msdn.microsoft.com/9de29d43-0677-4dc9-927f-af7c01179991">MI_Application_NewSerializer</a>
 

 

