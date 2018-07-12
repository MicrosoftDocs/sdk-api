---
UID: NF:mi.MI_DestinationOptions_Clone
title: MI_DestinationOptions_Clone function
author: windows-sdk-content
description: Creates a copy of a MI_DestinationOptions structure.
old-location: wmi_v2\mi_destinationoptions_clone.htm
old-project: wmi_v2
ms.assetid: f331561b-97ad-42f1-91b3-d180db92da07
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: MI_DestinationOptions_Clone, MI_DestinationOptions_Clone function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_Clone, wmi_v2.mi_destinationoptions_clone
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
 - MI_DestinationOptions_Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_DestinationOptions_Clone function


## -description


Creates a copy of a <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> structure.


## -parameters




### -param self [in]


<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> structure to be cloned.


### -param newDestinationOptions [out]

A pointer to the returned <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> clone. The cloned copy must be closed with the <a href="https://msdn.microsoft.com/c4cc8622-1adb-4e91-877f-11a260ca4bd7">MI_DestinationOptions_Delete</a> function.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.



