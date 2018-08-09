---
UID: NF:mi.MI_DestinationOptions_SetImpersonationType
title: MI_DestinationOptions_SetImpersonationType function
author: windows-sdk-content
description: Sets the impersonation type.
old-location: wmi_v2\mi_destinationoptions_setimpersonationtype.htm
old-project: wmi_v2
ms.assetid: f52370cb-b26c-4f0f-9869-1207c906e4e8
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_DestinationOptions_SetImpersonationType, MI_DestinationOptions_SetImpersonationType function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetImpersonationType, wmi_v2.mi_destinationoptions_setimpersonationtype
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
 - MI_DestinationOptions_SetImpersonationType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_DestinationOptions_SetImpersonationType function


## -description


Sets the impersonation type.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from the <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a> function.


### -param impersonationType [in]


<a href="https://msdn.microsoft.com/3d78ca66-8807-45b2-8648-bc5b0dfb83c6">MI_DestinationOptions_ImpersonationType</a> enumeration.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



