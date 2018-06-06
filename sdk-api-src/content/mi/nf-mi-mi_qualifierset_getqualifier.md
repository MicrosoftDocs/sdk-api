---
UID: NF:mi.MI_QualifierSet_GetQualifier
title: MI_QualifierSet_GetQualifier function
author: windows-sdk-content
description: Gets the qualifier information based on the given qualifier name.
old-location: wmi_v2\mi_qualifierset_getqualifier.htm
old-project: wmi_v2
ms.assetid: 16dde421-3746-4722-9f08-56835b7603fb
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_QualifierSet_GetQualifier, MI_QualifierSet_GetQualifier function [Windows Management Infrastructure (MI)], mi/MI_QualifierSet_GetQualifier, wmi_v2.mi_qualifierset_getqualifier
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
 - MI_QualifierSet_GetQualifier
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_QualifierSet_GetQualifier function


## -description


Gets the qualifier information based on the given qualifier name.


## -parameters




### -param self [in]


<a href="https://msdn.microsoft.com/6c374d19-c433-4c70-a644-e53a401f96dd">MI_QualifierSet</a> structure.


### -param name

A null-terminated string that represents the name of the qualifier to get.


### -param qualifierType [out]

Returned qualifier type.


### -param qualifierFlags [out]

Returned qualifier flags that indicate the scope of a qualifier.


### -param qualifierValue [out]

Returned qualifier value. This value has the lifetime of the qualifier set.


### -param index [out]

Returned zero-based index of the qualifier.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



