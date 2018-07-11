---
UID: NS:ndhelper.tagHYPOTHESIS
title: tagHYPOTHESIS
author: windows-sdk-content
description: The HYPOTHESIS structure contains data used to submit a hypothesis to NDF for another helper class.
old-location: ndf\hypothesis.htm
old-project: ndf
ms.assetid: 8f137633-8501-404c-9540-d558be9beeca
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PHYPOTHESIS, HYPOTHESIS, HYPOTHESIS structure [NDF], HYPOTHESIS,*PHYPOTHESIS, HYPOTHESIS,*PHYPOTHESIS structure [NDF], ndf.hypothesis, ndhelper/HYPOTHESIS, tagHYPOTHESIS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ndhelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ndhelper.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: HYPOTHESIS, *PHYPOTHESIS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndhelper.h
api_name:
 - HYPOTHESIS, *PHYPOTHESIS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagHYPOTHESIS structure


## -description


The <b>HYPOTHESIS</b> structure contains data used to submit a hypothesis to NDF for another  helper class. The name of the helper class, the number of parameters that the helper class requires, and the parameters to pass to the helper class are contained in this structure.


## -struct-fields




### -field pwszClassName

Type: <b>[string] LPWSTR</b>

A pointer to a null-terminated string that contains the name of the helper class.


### -field pwszDescription

Type: <b>[string] LPWSTR</b>

A  pointer to a null-terminated string that contains a user-friendly description of the data being passed to the helper class..


### -field celt

Type: <b>ULONG</b>

The count of attributes in this hypothesis.


### -field rgAttributes

Type: <b>[size_is(celt)]PHELPER_ATTRIBUTE[ ]</b>

A pointer to an array of <a href="https://msdn.microsoft.com/bff9303e-7fab-49af-b213-aa0a9c83676e">HELPER_ATTRIBUTE</a> structures that contains key attributes for this hypothesis. 


## -see-also




<a href="https://msdn.microsoft.com/bff9303e-7fab-49af-b213-aa0a9c83676e">HELPER_ATTRIBUTE</a>
 

 

