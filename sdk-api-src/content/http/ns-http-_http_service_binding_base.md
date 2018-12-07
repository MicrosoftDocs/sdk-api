---
UID: NS:http._HTTP_SERVICE_BINDING_BASE
title: "_HTTP_SERVICE_BINDING_BASE"
author: windows-sdk-content
description: HTTP_SERVICE_BINDING_BASE.
old-location: http\http_service_binding_base.htm
tech.root: http
ms.assetid: c9d3ed21-8987-4b98-99a1-dc1e776b0dab
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PHTTP_SERVICE_BINDING_BASE, HTTP_SERVICE_BINDING_BASE, HTTP_SERVICE_BINDING_BASE structure [HTTP], PHTTP_SERVICE_BINDING_BASE, PHTTP_SERVICE_BINDING_BASE structure pointer [HTTP], _HTTP_SERVICE_BINDING_BASE, http.http_service_binding_base, http/HTTP_SERVICE_BINDING_BASE, http/PHTTP_SERVICE_BINDING_BASE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Http.h
api_name:
 - HTTP_SERVICE_BINDING_BASE
product: Windows
targetos: Windows
req.typenames: HTTP_SERVICE_BINDING_BASE, *PHTTP_SERVICE_BINDING_BASE
req.redist: 
---

# _HTTP_SERVICE_BINDING_BASE structure


## -description


The <b>HTTP_SERVICE_BINDING_BASE</b> structure is a placeholder for the <a href="https://msdn.microsoft.com/bad1a042-fda8-4a2a-a8c1-26ed1f87c442">HTTP_SERVICE_BINDING_A</a> structure and the <a href="https://msdn.microsoft.com/0d840097-82d3-4ee3-b0d9-bcac4cf3e935">HTTP_SERVICE_BINDING_W</a> structure.


## -struct-fields




### -field Type

Pointer to an <a href="https://msdn.microsoft.com/8de36795-c99d-46ce-b9e4-a933de7d4c5c">HTTP_SERVICE_BINDING_TYPE</a> value that indicates whether the data is in ASCII or Unicode.


## -remarks



<div class="alert"><b>Note</b>  <p class="note">The first member of both the  <a href="https://msdn.microsoft.com/bad1a042-fda8-4a2a-a8c1-26ed1f87c442">HTTP_SERVICE_BINDING_A</a> structure and the <a href="https://msdn.microsoft.com/0d840097-82d3-4ee3-b0d9-bcac4cf3e935">HTTP_SERVICE_BINDING_W</a> structure is a <b>HTTP_SERVICE_BINDING_BASE</b> structure.  Therefore, an array of either of the first two structures can be indicated by a pointer to a <b>HTTP_SERVICE_BINDING_BASE</b> structure.

<p class="note">The <b>ServiceNames</b> member of the <a href="https://msdn.microsoft.com/60428e66-9c08-418b-99e1-6824c638f2be">HTTP_CHANNEL_BIND_INFO</a> structure is cast to a  pointer to a <b>HTTP_SERVICE_BINDING_BASE</b> structure for this purpose.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/60428e66-9c08-418b-99e1-6824c638f2be">HTTP_CHANNEL_BIND_INFO</a>



<a href="https://msdn.microsoft.com/bad1a042-fda8-4a2a-a8c1-26ed1f87c442">HTTP_SERVICE_BINDING_A</a>



<a href="https://msdn.microsoft.com/8de36795-c99d-46ce-b9e4-a933de7d4c5c">HTTP_SERVICE_BINDING_TYPE</a>



<a href="https://msdn.microsoft.com/0d840097-82d3-4ee3-b0d9-bcac4cf3e935">HTTP_SERVICE_BINDING_W</a>
 

 

