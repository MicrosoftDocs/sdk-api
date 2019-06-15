---
UID: NS:dwrite.DWRITE_SCRIPT_ANALYSIS
title: DWRITE_SCRIPT_ANALYSIS (dwrite.h)
author: windows-sdk-content
description: Stores the association of text and its writing system script, as well as some display attributes.
old-location: directwrite\dwrite_script_analysis.htm
tech.root: DirectWrite
ms.assetid: dafda5f6-39aa-4577-9213-898bdeddc7c2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DWRITE_SCRIPT_ANALYSIS, DWRITE_SCRIPT_ANALYSIS structure [Direct Write], directwrite.dwrite_script_analysis, dwrite/DWRITE_SCRIPT_ANALYSIS
ms.topic: struct
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - dwrite.h
api_name:
 - DWRITE_SCRIPT_ANALYSIS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DWRITE_SCRIPT_ANALYSIS structure


## -description


Stores the association of text and its writing system script, as well as some display attributes.


## -struct-fields




### -field script

Type: <b>UINT16</b>

The zero-based index representation of writing system script.


### -field shapes

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dwrite/ne-dwrite-dwrite_script_shapes">DWRITE_SCRIPT_SHAPES</a></b>

A value that indicates additional shaping requirement of text.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript">IDWriteTextAnalyzer::AnalyzeScript</a>
 

 

