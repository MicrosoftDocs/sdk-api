---
UID: NF:d2d1effectauthor.ID2D1AnalysisTransform.ProcessAnalysisResults
title: ID2D1AnalysisTransform::ProcessAnalysisResults
author: windows-sdk-content
description: Supplies the analysis data to an analysis transform.
old-location: direct2d\id2d1analysistransform_processanalysisresults.htm
tech.root: direct2d
ms.assetid: 3E7D8CDB-C3A0-4167-BDD4-66376D81BE41
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: ID2D1AnalysisTransform interface [Direct2D],ProcessAnalysisResults method, ID2D1AnalysisTransform.ProcessAnalysisResults, ID2D1AnalysisTransform::ProcessAnalysisResults, ProcessAnalysisResults, ProcessAnalysisResults method [Direct2D], ProcessAnalysisResults method [Direct2D],ID2D1AnalysisTransform interface, d2d1effectauthor/ID2D1AnalysisTransform::ProcessAnalysisResults, direct2d.id2d1analysistransform_processanalysisresults
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1AnalysisTransform.ProcessAnalysisResults
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1AnalysisTransform::ProcessAnalysisResults


## -description


Supplies the analysis data to an analysis transform.


## -parameters




### -param analysisData [in]

Type: <b>const BYTE*</b>

The data that the transform will analyze.


### -param analysisDataCount

Type: <b>UINT</b>

The size of the analysis data.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The output of the transform will be copied to CPU-accessible memory by the imaging effects system before being passed to the implementation.

 If this call fails, the corresponding <a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a> instance is placed into an error state and fails to draw.




## -see-also




<a href="https://msdn.microsoft.com/64CDA0A7-2790-436C-9EFC-3A74D09602B9">ID2D1AnalysisTransform</a>



<a href="https://msdn.microsoft.com/265888DA-03C2-42F0-92D8-FEB542F9BAA4">ID2D1EffectContext::CreateResourceTexture</a>
 

 

