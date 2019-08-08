---
UID: NF:mi.MI_DestinationOptions_Clone
title: MI_DestinationOptions_Clone function (mi.h)
author: windows-sdk-content
description: Creates a copy of a MI_DestinationOptions structure.
old-location: wmi_v2\mi_destinationoptions_clone.htm
tech.root: wmi_v2
ms.assetid: f331561b-97ad-42f1-91b3-d180db92da07
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_Clone, MI_DestinationOptions_Clone function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_Clone, wmi_v2.mi_destinationoptions_clone
ms.topic: function
f1_keywords:
- mi/MI_DestinationOptions_Clone
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
- MI_DestinationOptions_Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_DestinationOptions_Clone function


## -description


Creates a copy of a <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> structure.


## -parameters




### -param self [in]


<a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> structure to be cloned.


### -param newDestinationOptions [out]

A pointer to the returned <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> clone. The cloned copy must be closed with the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_delete">MI_DestinationOptions_Delete</a> function.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.



