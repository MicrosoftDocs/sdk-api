---
UID: NS:mprapi._PPP_ATCP_INFO
title: "_PPP_ATCP_INFO"
author: windows-sdk-content
description: The PPP_ATCP_INFO structure contains the result of a PPP AppleTalk projection operation.
old-location: rras\ppp_atcp_info.htm
old-project: rras
ms.assetid: 48d2404b-df8d-4ed0-9203-921474c88551
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PPP_ATCP_INFO, PPP_ATCP_INFO structure [RAS], _PPP_ATCP_INFO, _mpr_ppp_atcp_info, mprapi/PPP_ATCP_INFO, rras.ppp_atcp_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: PPP_ATCP_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - PPP_ATCP_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _PPP_ATCP_INFO structure


## -description


The 
<b>PPP_ATCP_INFO</b> structure contains the result of a PPP AppleTalk projection operation.


## -struct-fields




### -field dwError

Specifies the result of the PPP control protocol negotiation. A value of zero indicates success. A nonzero value indicates failure, and is the actual fatal error that occurred during the control protocol negotiation.


### -field wszAddress

Specifies a Unicode string that holds the client's AppleTalk address on the RAS connection.


## -see-also




<a href="https://msdn.microsoft.com/39692a38-ab40-43da-a704-8c206be72ceb">PPP_INFO</a>



<a href="https://msdn.microsoft.com/858fcdd8-6587-41c4-a2d7-c871722562e7">RAS Administration Structures</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

