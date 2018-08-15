---
UID: NS:lpmapi.IS_FLOWSPEC
title: IS_FLOWSPEC
author: windows-sdk-content
description: The IS_FLOWSPEC structure stores an Integrated Services FLOWSPEC object.
old-location: qos\is_flowspec.htm
old-project: qos
ms.assetid: 1e0cd196-f53c-4d68-a287-7a98b7215d6d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IS_FLOWSPEC, IS_FLOWSPEC structure [QOS], lpmapi/IS_FLOWSPEC, qos.is_flowspec
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lpmapi.h
req.include-header: 
req.redist: 
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
req.typenames: IS_FLOWSPEC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - IS_FLOWSPEC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IS_FLOWSPEC structure


## -description


The 
<b>IS_FLOWSPEC</b> structure stores an Integrated Services FLOWSPEC object.


## -struct-fields




### -field flow_header

General information and length information for the Integrated Services flowspec object (this structure), expressed as an <a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a> structure.


### -field flow_body

FLOWSPEC object data, expressed as an <a href="https://msdn.microsoft.com/c16115ba-03fa-4363-bf16-5341da54f792">IntServFlowSpec</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/c16115ba-03fa-4363-bf16-5341da54f792">IntServFlowSpec</a>



<a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a>
 

 

