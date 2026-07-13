---
UID: NN:comsvcs.ICrmCompensator
title: ICrmCompensator (comsvcs.h)
description: Delivers unstructured log records to the CRM Compensator when using Microsoft Visual C++.
helpviewer_keywords: ["ICrmCompensator","ICrmCompensator interface [COM+]","ICrmCompensator interface [COM+]","described","_dtc_ICrmCompensator_Interface","comsvcs/ICrmCompensator","cos.icrmcompensator"]
old-location: cos\icrmcompensator.htm
tech.root: cos
ms.assetid: 9e5a8f2c-4115-42bd-a541-d0ce75c45b72
ms.date: 12/05/2018
ms.keywords: ICrmCompensator, ICrmCompensator interface [COM+], ICrmCompensator interface [COM+],described, _dtc_ICrmCompensator_Interface, comsvcs/ICrmCompensator, cos.icrmcompensator
req.header: comsvcs.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICrmCompensator
 - comsvcs/ICrmCompensator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmCompensator
---

# ICrmCompensator interface


## -description

Delivers unstructured log records to the CRM Compensator when using Microsoft Visual C++.

## -inheritance

The <b>ICrmCompensator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICrmCompensator</b> also has these types of members:

## -remarks

The CRM clerk determines the CLSID of the CRM Compensator using the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmlogcontrol-registercompensator">ICrmLogControl::RegisterCompensator</a> method. It next calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> specifying the CLSID of this CRM Compensator, and then it calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for both the <b>ICrmCompensator</b> interface and the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensatorvariants">ICrmCompensatorVariants</a> interface.

## -see-also

<a href="/windows/desktop/cossdk/com--compensating-resource-manager">COM+ Compensating Resource Manager</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensatorvariants">ICrmCompensatorVariants</a>
