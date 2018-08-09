---
UID: NS:lpmapi.SENDER_TSPEC
title: SENDER_TSPEC
author: windows-sdk-content
description: The SENDER_TSPEC structure contains information for an RSVP sender Tspec.
old-location: qos\sender_tspec.htm
old-project: qos
ms.assetid: d7905687-1af8-4469-b8de-a2445afa90f4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SENDER_TSPEC, SENDER_TSPEC structure [QOS], lpmapi/SENDER_TSPEC, qos.sender_tspec
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lpmapi.h
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
req.typenames: SENDER_TSPEC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - SENDER_TSPEC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# SENDER_TSPEC structure


## -description


The 
<b>SENDER_TSPEC</b> structure contains information for an RSVP sender Tspec.


## -struct-fields




### -field stspec_header

Object header, expressed as an <a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a> structure.


### -field stspec_body

Sender Tspec body information, expressed as an <a href="https://msdn.microsoft.com/c4244dba-237a-437b-94b7-fd814edb3506">IntServTspecBody</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/c4244dba-237a-437b-94b7-fd814edb3506">IntServTspecBody</a>



<a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a>
 

 

