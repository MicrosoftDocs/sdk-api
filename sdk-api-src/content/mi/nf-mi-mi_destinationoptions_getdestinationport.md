---
UID: NF:mi.MI_DestinationOptions_GetDestinationPort
title: MI_DestinationOptions_GetDestinationPort function (mi.h)
description: Gets the default port for transport.helpviewer_keywords: ["MI_DestinationOptions_GetDestinationPort","MI_DestinationOptions_GetDestinationPort function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_GetDestinationPort","wmi_v2.mi_destinationoptions_getdestinationport"]
old-location: wmi_v2\mi_destinationoptions_getdestinationport.htm
tech.root: wmi_v2
ms.assetid: 49621cd8-a4ce-45b3-a20e-ecdef220d7e4
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_GetDestinationPort, MI_DestinationOptions_GetDestinationPort function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetDestinationPort, wmi_v2.mi_destinationoptions_getdestinationport
f1_keywords:
- mi/MI_DestinationOptions_GetDestinationPort
dev_langs:
- c++
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
- MI_DestinationOptions_GetDestinationPort
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_DestinationOptions_GetDestinationPort function


## -description


Gets the default port for transport.


## -parameters




### -param options [in]


<a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>.


### -param port [out]

Returned port number.


## -returns



A value of the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



