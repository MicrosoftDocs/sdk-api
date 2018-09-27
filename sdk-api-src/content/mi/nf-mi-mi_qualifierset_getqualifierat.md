---
UID: NF:mi.MI_QualifierSet_GetQualifierAt
title: MI_QualifierSet_GetQualifierAt function
author: windows-sdk-content
description: Gets a qualifier at the specified index.
old-location: wmi_v2\mi_qualifierset_getqualifierat.htm
tech.root: WMI_v2
ms.assetid: 5dfcdd7a-7740-4d40-b412-89f6f090561c
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: MI_QualifierSet_GetQualifierAt, MI_QualifierSet_GetQualifierAt function [Windows Management Infrastructure (MI)], mi/MI_QualifierSet_GetQualifierAt, wmi_v2.mi_qualifierset_getqualifierat
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_QualifierSet_GetQualifierAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_QualifierSet_GetQualifierAt function


## -description


Gets a qualifier at the specified index.


## -parameters




### -param self [in]


<a href="https://msdn.microsoft.com/6c374d19-c433-4c70-a644-e53a401f96dd">MI_QualifierSet</a> structure.


### -param index

Zero-based index of the qualifier to get.


### -param name

Returned qualifier name.


### -param qualifierType [out]

Returned qualifier type.


### -param qualifierFlags [out]

Returned qualifier flags.


### -param qualifierValue [out]

Returned qualifier value. This value has the same scope as the qualifier set.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



