---
UID: NF:mi.MI_PropertySet_ContainsElement
title: MI_PropertySet_ContainsElement function
author: windows-sdk-content
description: Determines whether the property list contains the specified property name.
old-location: wmi_v2\mi_propertyset_containselement.htm
old-project: wmi_v2
ms.assetid: 71cf9c53-4e97-432c-9dfe-bef8ba119f71
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_PropertySet_ContainsElement, MI_PropertySet_ContainsElement function [Windows Management Infrastructure (MI)], mi/MI_PropertySet_ContainsElement, wmi_v2.mi_propertyset_containselement
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
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_PropertySet_ContainsElement
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_PropertySet_ContainsElement function


## -description


Determines whether the property list contains the specified property name.


## -parameters




### -param self [in]

Property list to be checked.


### -param name

A null-terminated string that represents the name to check for in the property list.


### -param flag [out]

Returned Boolean value. <b>MI_TRUE</b> indicates that the specified property was found; otherwise <b>MI_FALSE</b> is returned.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



