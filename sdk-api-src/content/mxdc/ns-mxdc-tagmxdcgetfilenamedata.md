---
UID: NS:mxdc.tagMxdcGetFileNameData
title: tagMxdcGetFileNameData
author: windows-driver-content
description: The MXDC_GET_FILENAME_DATA_T structure holds the full path and file name of a Microsoft XPS Document Converter (MXDC) output file.
old-location: gdi\mxdcgetfilenamedata.htm
old-project: printdocs
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*P_MXDC_GET_FILENAME_DATA_T, MXDC_GET_FILENAME_DATA_T, MXDC_GET_FILENAME_DATA_T structure [Windows GDI], P_MXDC_GET_FILENAME_DATA_T, P_MXDC_GET_FILENAME_DATA_T structure pointer [Windows GDI], _win32_tagMxdcGetFileNameData_str, gdi.mxdcgetfilenamedata, mxdc/MXDC_GET_FILENAME_DATA_T, mxdc/P_MXDC_GET_FILENAME_DATA_T, tagMxdcGetFileNameData"
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
req.typenames: MXDC_GET_FILENAME_DATA_T, *P_MXDC_GET_FILENAME_DATA_T
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mxdc.h
api_name:
-	MXDC_GET_FILENAME_DATA_T
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagMxdcGetFileNameData structure


## -description



The <b>MXDC_GET_FILENAME_DATA_T</b> structure holds the full path and file name of a Microsoft XPS Document Converter (MXDC) output file.




## -struct-fields




### -field cbOutput

The size of the output buffer, <b>wszData</b>.


### -field wszData

The fully qualified path and file name of the output file.


## -remarks



This structure is returned by <a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a> when it is called with the <a href="https://msdn.microsoft.com/79aeb32e-94b1-4806-8ebf-a9d0956f4667">MXDC_ESCAPE</a> escape and the <a href="https://msdn.microsoft.com/3d1f909c-0c3c-49ac-b530-4ce077ad6d94">MXDC_ESCAPE_HEADER_T</a> structure that is passed in the <i>lpszInData</i> parameter has its <b>opCode</b> set to <b>MXDCOP_GET_FILENAME</b>.




## -see-also




<a href="https://msdn.microsoft.com/5ca74f61-75dd-4a8c-9f0f-9c1b4719c75f">ExtEscape</a>



<a href="https://msdn.microsoft.com/1e54b151-2324-4d6b-975a-feb42c37b18d">GDI Printer Escape Functions</a>



<a href="https://msdn.microsoft.com/79aeb32e-94b1-4806-8ebf-a9d0956f4667">MXDC_ESCAPE</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

