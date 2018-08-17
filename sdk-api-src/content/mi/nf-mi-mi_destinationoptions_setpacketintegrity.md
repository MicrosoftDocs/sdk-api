---
UID: NF:mi.MI_DestinationOptions_SetPacketIntegrity
title: MI_DestinationOptions_SetPacketIntegrity function
author: windows-sdk-content
description: Enables or disables packet integrity (signing) of a protocol connection.
old-location: wmi_v2\mi_destinationoptions_setpacketintegrity.htm
old-project: wmi_v2
ms.assetid: 62980401-84ba-40af-a0c0-36d24c4d68f4
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: MI_DestinationOptions_SetPacketIntegrity, MI_DestinationOptions_SetPacketIntegrity function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetPacketIntegrity, wmi_v2.mi_destinationoptions_setpacketintegrity
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
 - MI_DestinationOptions_SetPacketIntegrity
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_DestinationOptions_SetPacketIntegrity function


## -description


Enables or disables packet integrity (signing) of a protocol connection.


## -parameters




### -param options [in, out]

A <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from the <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a> function.


### -param integrity

Boolean value where <b>MI_TRUE</b> means to use packet integrity (signing) and <b>MI_FALSE</b> means to not use packet integrity.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



The default setting is <b>MI_TRUE</b>. This setting does not apply to all protocols and will be ignored when not supported.



