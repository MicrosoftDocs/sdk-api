---
UID: NF:mi.MI_DestinationOptions_SetPacketEncoding
title: MI_DestinationOptions_SetPacketEncoding function (mi.h)
description: Sets the encoding mechanism for certain protocol handles.
helpviewer_keywords: ["MI_DESTINATIONOPTIONS_PACKET_ENCODING_DEFAULT","MI_DESTINATIONOPTIONS_PACKET_ENCODING_UTF16","MI_DESTINATIONOPTIONS_PACKET_ENCODING_UTF8","MI_DestinationOptions_SetPacketEncoding","MI_DestinationOptions_SetPacketEncoding function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_SetPacketEncoding","wmi_v2.mi_destinationoptions_setpacketencoding"]
old-location: wmi_v2\mi_destinationoptions_setpacketencoding.htm
tech.root: wmi_v2
ms.assetid: cb7f922d-7e96-4304-9abe-bfa23709e1c7
ms.date: 12/05/2018
ms.keywords: MI_DESTINATIONOPTIONS_PACKET_ENCODING_DEFAULT, MI_DESTINATIONOPTIONS_PACKET_ENCODING_UTF16, MI_DESTINATIONOPTIONS_PACKET_ENCODING_UTF8, MI_DestinationOptions_SetPacketEncoding, MI_DestinationOptions_SetPacketEncoding function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetPacketEncoding, wmi_v2.mi_destinationoptions_setpacketencoding
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
 - MI_DestinationOptions_SetPacketEncoding
 - mi/MI_DestinationOptions_SetPacketEncoding
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
 - MI_DestinationOptions_SetPacketEncoding
---

# MI_DestinationOptions_SetPacketEncoding function


## -description

Sets the encoding mechanism for certain protocol handles.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a> function.

### -param encoding

A null-terminated string representing one of the following encoding mechanism values.



#### MI_DESTINATIONOPTIONS_PACKET_ENCODING_DEFAULT ("default")

Transport-specific default encoding per the WinRM protocol handler.



#### MI_DESTINATIONOPTIONS_PACKET_ENCODING_UTF8 ("UTF8")

UTF-8 encoding.



#### MI_DESTINATIONOPTIONS_PACKET_ENCODING_UTF16 ("UTF16")

UTF-16 encoding.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_getpacketencoding">MI_DestinationOptions_GetPacketEncoding</a>



<a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>