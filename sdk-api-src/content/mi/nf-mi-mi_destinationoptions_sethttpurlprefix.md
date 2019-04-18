---
UID: NF:mi.MI_DestinationOptions_SetHttpUrlPrefix
title: MI_DestinationOptions_SetHttpUrlPrefix function (mi.h)
author: windows-sdk-content
description: Set the default HTTP URL prefix for transports that go over HTTP and HTTPS.
old-location: wmi_v2\mi_destinationoptions_sethttpurlprefix.htm
tech.root: wmi_v2
ms.assetid: fc5b6dd8-3243-49b4-a8da-8351a9c3f209
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_SetHttpUrlPrefix, MI_DestinationOptions_SetHttpUrlPrefix function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetHttpUrlPrefix, wmi_v2.mi_destinationoptions_sethttpurlprefix
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
 - MI_DestinationOptions_SetHttpUrlPrefix
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_DestinationOptions_SetHttpUrlPrefix function


## -description


Set the default HTTP URL prefix for transports that go over HTTP and HTTPS.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from the <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a> function.


### -param prefix

A null-terminated string that represents the HTTP URL prefix ("HTTP" or "HTTPS").


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



The default URL prefix is protocol specific.  This setting is ignored by transports that do not support this.




## -see-also




<a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>



<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a>



<a href="https://msdn.microsoft.com/4e933485-e489-4185-9879-356a4e567a48">MI_DestinationOptions_GetHttpUrlPrefix</a>



<a href="https://msdn.microsoft.com/85e0a952-c51c-4877-b9fb-d2fe0d0b1bb1">MI_DestinationOptions_GetTransport</a>



<a href="https://msdn.microsoft.com/998ac6ee-29a4-49bf-8ca1-01b7afddd33f">MI_DestinationOptions_SetTransport</a>
 

 

