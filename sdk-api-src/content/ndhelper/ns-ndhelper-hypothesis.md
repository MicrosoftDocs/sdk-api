---
UID: NS:ndhelper.tagHYPOTHESIS
title: HYPOTHESIS (ndhelper.h)
description: The HYPOTHESIS structure contains data used to submit a hypothesis to NDF for another helper class.
helpviewer_keywords: ["*PHYPOTHESIS","HYPOTHESIS","HYPOTHESIS structure [NDF]","HYPOTHESIS","*PHYPOTHESIS","HYPOTHESIS","*PHYPOTHESIS structure [NDF]","ndf.hypothesis","ndhelper/HYPOTHESIS"]
old-location: ndf\hypothesis.htm
tech.root: NDF
ms.assetid: 8f137633-8501-404c-9540-d558be9beeca
ms.date: 12/05/2018
ms.keywords: '*PHYPOTHESIS, HYPOTHESIS, HYPOTHESIS structure [NDF], HYPOTHESIS,*PHYPOTHESIS, HYPOTHESIS,*PHYPOTHESIS structure [NDF], ndf.hypothesis, ndhelper/HYPOTHESIS'
req.header: ndhelper.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: HYPOTHESIS, *PHYPOTHESIS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHYPOTHESIS
 - ndhelper/tagHYPOTHESIS
 - PHYPOTHESIS
 - ndhelper/PHYPOTHESIS
 - HYPOTHESIS
 - ndhelper/HYPOTHESIS
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
 - HYPOTHESIS, *PHYPOTHESIS
---

# HYPOTHESIS structure


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

A pointer to an array of <a href="/windows/desktop/api/ndattrib/ns-ndattrib-helper_attribute">HELPER_ATTRIBUTE</a> structures that contains key attributes for this hypothesis.

## -see-also

<a href="/windows/desktop/api/ndattrib/ns-ndattrib-helper_attribute">HELPER_ATTRIBUTE</a>