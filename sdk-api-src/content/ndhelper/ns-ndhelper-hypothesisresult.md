---
UID: NS:ndhelper.tagHypothesisResult
title: HypothesisResult (ndhelper.h)
description: Contains information about a hypothesis returned from a helper class.
helpviewer_keywords: ["HypothesisResult","HypothesisResult structure [NDF]","ndf.hypothesisresult","ndhelper/HypothesisResult"]
old-location: ndf\hypothesisresult.htm
tech.root: NDF
ms.assetid: bbf3cc69-c81b-4a3d-8fd8-d4e37a57bed6
ms.date: 12/05/2018
ms.keywords: HypothesisResult, HypothesisResult structure [NDF], ndf.hypothesisresult, ndhelper/HypothesisResult
req.header: ndhelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ndhelper.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: HypothesisResult
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHypothesisResult
 - ndhelper/tagHypothesisResult
 - HypothesisResult
 - ndhelper/HypothesisResult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndhelper.h
api_name:
 - HypothesisResult
---

# HypothesisResult structure


## -description

The <b>HypothesisResult</b> structure contains information about a hypothesis returned from a helper class. The hypothesis is obtained via a call to <a href="/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getlowerhypotheses">GetLowerHypotheses</a>.

## -struct-fields

### -field hypothesis

Type: <b><a href="/windows/desktop/api/ndhelper/ns-ndhelper-hypothesis">HYPOTHESIS</a></b>

Information for a specific hypothesis.

### -field pathStatus

Type: <b><a href="/windows/desktop/api/ndhelper/ne-ndhelper-diagnosis_status">DIAGNOSIS_STATUS</a></b>

The status of the child helper class and its children. 

If the hypothesis or any of its children indicated <b>DS_CONFIRMED</b> in a call to <a href="/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth">LowHealth</a>, then this value will be <b>DS_CONFIRMED</b>. If no problems exist in such a call, the value will be <b>DS_REJECTED</b>. The value will be <b>DS_INDETERMINATE</b> if the health of the component is not clear.

## -see-also

<a href="/windows/desktop/api/ndhelper/ne-ndhelper-diagnosis_status">DIAGNOSIS_STATUS</a>



<a href="/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getlowerhypotheses">GetLowerHypotheses</a>



<a href="/windows/desktop/api/ndhelper/ns-ndhelper-hypothesis">HYPOTHESIS</a>



<a href="/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth">LowHealth</a>