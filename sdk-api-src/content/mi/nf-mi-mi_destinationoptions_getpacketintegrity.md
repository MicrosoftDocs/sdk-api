---
UID: NF:mi.MI_DestinationOptions_GetPacketIntegrity
title: MI_DestinationOptions_GetPacketIntegrity function
author: windows-sdk-content
description: Gets the packet integrity setting.
old-location: wmi_v2\mi_destinationoptions_getpacketintegrity.htm
old-project: wmi_v2
ms.assetid: 7f30822b-38c4-4d5e-b176-59aa403fa3fa
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: MI_DestinationOptions_GetPacketIntegrity, MI_DestinationOptions_GetPacketIntegrity function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetPacketIntegrity, wmi_v2.mi_destinationoptions_getpacketintegrity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mi.h
req.include-header: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
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
 - MI_DestinationOptions_GetPacketIntegrity
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_DestinationOptions_GetPacketIntegrity function


## -description


Gets the packet integrity setting.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>.


### -param integrity [out]

The returned Boolean value. If this value is <b>MI_TRUE</b>, the session contains protection against tampering.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



