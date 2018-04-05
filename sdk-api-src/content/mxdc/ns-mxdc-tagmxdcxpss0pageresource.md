---
UID: NS:mxdc.tagMxdcXpsS0PageResource
title: tagMxdcXpsS0PageResource
author: windows-driver-content
description: The MXDC_XPS_S0PAGE_RESOURCE_T structure holds information about a resource, such as an image or font, that is associated with an XPS document page, and is to be passed to the Microsoft XPS Document Converter (MXDC) output file.
old-location: gdi\mxdcxpss0pageresource.htm
old-project: printdocs
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*P_MXDC_XPS_S0PAGE_RESOURCE_T, MXDC_XPS_S0PAGE_RESOURCE_T, MXDC_XPS_S0PAGE_RESOURCE_T structure [Windows GDI], P_MXDC_XPS_S0PAGE_RESOURCE_T, P_MXDC_XPS_S0PAGE_RESOURCE_T structure pointer [Windows GDI], _win32_tagMxdcXpsS0PageResource_str, gdi.mxdcxpss0pageresource, mxdc/MXDC_XPS_S0PAGE_RESOURCE_T, mxdc/P_MXDC_XPS_S0PAGE_RESOURCE_T, tagMxdcXpsS0PageResource"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mxdc.h
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
req.typenames: MXDC_XPS_S0PAGE_RESOURCE_T, *P_MXDC_XPS_S0PAGE_RESOURCE_T
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mxdc.h
api_name:
-	MXDC_XPS_S0PAGE_RESOURCE_T
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagMxdcXpsS0PageResource structure


## -description



The <b>MXDC_XPS_S0PAGE_RESOURCE_T</b> structure holds information about a resource, such as an image or font, that is associated with an XPS document page, and is to be passed to the Microsoft XPS Document Converter (MXDC) output file.




## -struct-fields




### -field dwSize

The total size of this structure and the resource to which it points.


### -field dwResourceType

A value of type <a href="https://msdn.microsoft.com/e111d92e-5102-4b39-b311-f9ff1d1a96f1">MXDC_S0_PAGE_ENUMS</a> indicating the type of resource, such as TIFF image or TrueType font.


### -field szUri

The URI of the resource. This cannot be more than 260 bytes.


### -field dwDataSize

The size of the resource in bytes.


### -field bData

The data of the resource in an array of bytes with size 1 + the size of the resource.


## -remarks



This structure is appended to a <a href="https://msdn.microsoft.com/3d1f909c-0c3c-49ac-b530-4ce077ad6d94">MXDC_ESCAPE_HEADER_T</a> structure (that has its <b>opCode</b> set to <b>MXDCOP_SET_S0PAGERESOURCE</b>) to make an <a href="https://msdn.microsoft.com/e5caa280-f0a5-4a89-b4f1-4f195a537dc6">MXDC_S0PAGE_RESOURCE_ESCAPE_T</a> structure. The resulting <b>MXDC_S0PAGE_RESOURCE_ESCAPE_T</b> structure is then passed in the <i>lpszInData</i> parameter of the <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> function that it is called with the <a href="https://msdn.microsoft.com/79aeb32e-94b1-4806-8ebf-a9d0956f4667">MXDC_ESCAPE</a> escape. The effect is to send the resource to the MXDC for conversion and to be written to the output file.

The call to <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> must be between a call to <a href="https://msdn.microsoft.com/library/windows/hardware/dn923219">StartPage</a> and a call to <a href="https://msdn.microsoft.com/33e6d005-f00d-4b87-bf7c-fc79c1d05514">EndPage</a>; however there can be more than one such calls between the calls to <b>StartPage</b> and <b>EndPage</b>.

Streaming consumption is more efficient if you call <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> with the <b>MXDCOP_SET_S0PAGE_RESOURCE</b> <b>opCode</b> for each resource on the page before you call <b>ExtEscape</b> with the <b>MXDCOP_SET_S0PAGE</b> <b>opCode</b>.




## -see-also




<a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a>



<a href="https://msdn.microsoft.com/1e54b151-2324-4d6b-975a-feb42c37b18d">GDI Printer Escape Functions</a>



<a href="https://msdn.microsoft.com/79aeb32e-94b1-4806-8ebf-a9d0956f4667">MXDC_ESCAPE</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

