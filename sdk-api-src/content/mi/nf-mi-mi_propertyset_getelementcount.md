---
UID: NF:mi.MI_PropertySet_GetElementCount
title: MI_PropertySet_GetElementCount function
author: windows-sdk-content
description: Gets the number of elements in the specified property set.
old-location: wmi_v2\mi_propertyset_getelementcount.htm
old-project: wmi_v2
ms.assetid: 450f778c-6b59-4c01-9c21-7f96f28ebe26
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_PropertySet_GetElementCount, MI_PropertySet_GetElementCount function [Windows Management Infrastructure (MI)], mi/MI_PropertySet_GetElementCount, wmi_v2.mi_propertyset_getelementcount
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_PropertySet_GetElementCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_PropertySet_GetElementCount function


## -description


Gets the number of elements in the specified property set.


## -parameters




### -param self [in]

Property set to enumerate.


### -param count [out]

Returned number of element in the property set.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



