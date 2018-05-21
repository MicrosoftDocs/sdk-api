---
UID: NF:mi.MI_DestinationOptions_SetPacketPrivacy
title: MI_DestinationOptions_SetPacketPrivacy function
author: windows-driver-content
description: Enables or disables packet privacy (encryption).
old-location: wmi_v2\mi_destinationoptions_setpacketprivacy.htm
old-project: wmi_v2
ms.assetid: bb047646-fa95-4691-946c-5faf5b7edc8b
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: MI_DestinationOptions_SetPacketPrivacy, MI_DestinationOptions_SetPacketPrivacy function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetPacketPrivacy, wmi_v2.mi_destinationoptions_setpacketprivacy
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
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_DestinationOptions_SetPacketPrivacy
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_DestinationOptions_SetPacketPrivacy function


## -description


Enables or disables packet privacy (encryption).


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from the <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a> function.


### -param privacy

Boolean value where <b>MI_TRUE</b> means to use encryption and <b>MI_FALSE</b> means to not use encryption.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



The default value for this setting is <b>MI_TRUE</b>.



