---
UID: NF:mi.MI_PropertySet_Clear
title: MI_PropertySet_Clear function
author: windows-sdk-content
description: Removes all names from the property list. Afterwards, the count is zero. This allows property lists to be reused (without having to be destructed and reconstructed).
old-location: wmi_v2\mi_propertyset_clear.htm
old-project: wmi_v2
ms.assetid: c5cd80b7-51bc-48dd-a49d-c3ce6d92fd55
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: MI_PropertySet_Clear, MI_PropertySet_Clear function [Windows Management Infrastructure (MI)], mi/MI_PropertySet_Clear, wmi_v2.mi_propertyset_clear
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
 - MI_PropertySet_Clear
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_PropertySet_Clear function


## -description


Removes all names from the property list. Afterwards, the count is zero. This allows property lists to be reused (without having to be destructed  and reconstructed).


## -parameters




### -param self [in, out]

Property list to clear.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



