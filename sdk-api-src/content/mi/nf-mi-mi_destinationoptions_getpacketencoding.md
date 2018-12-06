---
UID: NF:mi.MI_DestinationOptions_GetPacketEncoding
title: MI_DestinationOptions_GetPacketEncoding function
author: windows-sdk-content
description: Gets the previously set packet encoding setting.
old-location: wmi_v2\mi_destinationoptions_getpacketencoding.htm
tech.root: wmi_v2
ms.assetid: 8800ae5d-6776-4a06-bf1e-3ee621250856
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_DESTINATIONOPTIONS_PACKET_ENCODING_DEFAULT, MI_DESTINATIONOPTIONS_PACKET_ENCODING_UTF16, MI_DESTINATIONOPTIONS_PACKET_ENCODING_UTF8, MI_DestinationOptions_GetPacketEncoding, MI_DestinationOptions_GetPacketEncoding function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetPacketEncoding, wmi_v2.mi_destinationoptions_getpacketencoding
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
 - MI_DestinationOptions_GetPacketEncoding
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_DestinationOptions_GetPacketEncoding function


## -description


Gets the previously set packet encoding setting.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>.


### -param encoding

A pointer to a null-terminated string containing the returned encoding setting. Here are the possible values:



#### MI_DESTINATIONOPTIONS_PACKET_ENCODING_DEFAULT ("default")

Transport-specific default encoding per the WinRM protocol handler.



#### MI_DESTINATIONOPTIONS_PACKET_ENCODING_UTF8 ("UTF8")

UTF-8 encoding.



#### MI_DESTINATIONOPTIONS_PACKET_ENCODING_UTF16 ("UTF16")

UTF-16 encoding.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>
 

 

