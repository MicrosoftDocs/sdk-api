---
UID: NF:mi.MI_DestinationOptions_GetPacketPrivacy
title: MI_DestinationOptions_GetPacketPrivacy function
author: windows-sdk-content
description: Gets the packet privacy (encryption) setting.
old-location: wmi_v2\mi_destinationoptions_getpacketprivacy.htm
tech.root: wmi_v2
ms.assetid: 2abc5369-bb64-412b-a976-aac52aa5405b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MI_DestinationOptions_GetPacketPrivacy, MI_DestinationOptions_GetPacketPrivacy function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetPacketPrivacy, wmi_v2.mi_destinationoptions_getpacketprivacy
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
 - MI_DestinationOptions_GetPacketPrivacy
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
- apiref
: 
- 
: 
- MI_DestinationOptions_GetPacketPrivacy
: 
---

# MI_DestinationOptions_GetPacketPrivacy function


## -description


Gets the packet privacy (encryption) setting.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>.


### -param privacy [out]

The returned privacy (encryption) setting, a Boolean value. If this setting is <b>MI_TRUE</b>, then the session contains protection against eavesdropping.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



