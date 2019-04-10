---
UID: NS:lpmapi.__unnamed_struct_8
title: FILTER_SPEC (lpmapi.h)
author: windows-sdk-content
description: The FILTER_SPEC structure stores information about an RSVP FILTERSPEC.
old-location: qos\filter_spec.htm
tech.root: QOS
ms.assetid: 72d08944-7ac9-496f-a18b-e6fcddb59c56
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FILTER_SPEC, FILTER_SPEC structure [QOS], SENDER_TEMPLATE, lpmapi/FILTER_SPEC, qos.filter_spec
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - FILTER_SPEC
product: Windows
targetos: Windows
req.typenames: FILTER_SPEC
req.redist: 
---

# FILTER_SPEC structure


## -description


The 
<b>FILTER_SPEC</b> structure stores information about an RSVP FILTERSPEC.


## -struct-fields




### -field filt_header

RSVP Object Header for the FILTERSPEC, in the form of an <a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a> structure.


### -field filt_u



#### filt_ipv4

FILTERSPEC, in the form of a <a href="https://msdn.microsoft.com/b17a45b2-e50b-4ec2-9f1c-e1ab80ce572e">Filter_Spec_IPv4</a> header.



#### filt_ipv4gpi

FILTERSPEC GPI information, in the form of a <a href="https://msdn.microsoft.com/c1546673-d1b5-4a7f-82d0-a8cc1c7c8752">Filter_Spec_IPv4GPI</a> header.


### -field filt_ipv4

 


### -field filt_ipv4gpi

 




## -see-also




<a href="https://msdn.microsoft.com/b17a45b2-e50b-4ec2-9f1c-e1ab80ce572e">Filter_Spec_IPv4</a>



<a href="https://msdn.microsoft.com/c1546673-d1b5-4a7f-82d0-a8cc1c7c8752">Filter_Spec_IPv4GPI</a>



<a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a>
 

 

