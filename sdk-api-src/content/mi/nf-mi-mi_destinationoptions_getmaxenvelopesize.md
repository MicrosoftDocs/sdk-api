---
UID: NF:mi.MI_DestinationOptions_GetMaxEnvelopeSize
title: MI_DestinationOptions_GetMaxEnvelopeSize function (mi.h)
author: windows-sdk-content
description: Gets the maximum size of the packet sent to a server or received by the client from the server.
old-location: wmi_v2\mi_destinationoptions_getmaxenvelopesize.htm
tech.root: wmi_v2
ms.assetid: 103f5c77-3824-464b-9a0b-36e23ee98028
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_GetMaxEnvelopeSize, MI_DestinationOptions_GetMaxEnvelopeSize function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetMaxEnvelopeSize, wmi_v2.mi_destinationoptions_getmaxenvelopesize
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
 - MI_DestinationOptions_GetMaxEnvelopeSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_DestinationOptions_GetMaxEnvelopeSize function


## -description


Gets the maximum size of the packet sent to a server or received by the client from the server.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>.


### -param sizeInKB [out]

Returned packet size.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



