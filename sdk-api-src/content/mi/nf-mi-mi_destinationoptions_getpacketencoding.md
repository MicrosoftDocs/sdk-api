---
UID: NF:mi.MI_DestinationOptions_GetPacketEncoding
title: MI_DestinationOptions_GetPacketEncoding function (mi.h)
description: Gets the previously set packet encoding setting.
helpviewer_keywords: ["MI_DESTINATIONOPTIONS_PACKET_ENCODING_DEFAULT","MI_DESTINATIONOPTIONS_PACKET_ENCODING_UTF16","MI_DESTINATIONOPTIONS_PACKET_ENCODING_UTF8","MI_DestinationOptions_GetPacketEncoding","MI_DestinationOptions_GetPacketEncoding function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_GetPacketEncoding","wmi_v2.mi_destinationoptions_getpacketencoding"]
old-location: wmi_v2\mi_destinationoptions_getpacketencoding.htm
tech.root: wmi_v2
ms.assetid: 8800ae5d-6776-4a06-bf1e-3ee621250856
ms.date: 12/05/2018
ms.keywords: MI_DESTINATIONOPTIONS_PACKET_ENCODING_DEFAULT, MI_DESTINATIONOPTIONS_PACKET_ENCODING_UTF16, MI_DESTINATIONOPTIONS_PACKET_ENCODING_UTF8, MI_DestinationOptions_GetPacketEncoding, MI_DestinationOptions_GetPacketEncoding function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetPacketEncoding, wmi_v2.mi_destinationoptions_getpacketencoding
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
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_DestinationOptions_GetPacketEncoding
 - mi/MI_DestinationOptions_GetPacketEncoding
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_DestinationOptions_GetPacketEncoding
---

# MI_DestinationOptions_GetPacketEncoding function


## -description

Gets the previously set packet encoding setting.

## -parameters

### -param options [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>.

### -param encoding

A pointer to a null-terminated string containing the returned encoding setting. Here are the possible values:



#### MI_DESTINATIONOPTIONS_PACKET_ENCODING_DEFAULT ("default")

Transport-specific default encoding per the WinRM protocol handler.



#### MI_DESTINATIONOPTIONS_PACKET_ENCODING_UTF8 ("UTF8")

UTF-8 encoding.



#### MI_DESTINATIONOPTIONS_PACKET_ENCODING_UTF16 ("UTF16")

UTF-16 encoding.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>