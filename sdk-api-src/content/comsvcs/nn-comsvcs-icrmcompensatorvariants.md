---
UID: NN:comsvcs.ICrmCompensatorVariants
title: ICrmCompensatorVariants (comsvcs.h)
description: Delivers structured log records to the CRM Compensator when using Microsoft Visual Basic.
helpviewer_keywords: ["ICrmCompensatorVariants","ICrmCompensatorVariants interface [COM+]","ICrmCompensatorVariants interface [COM+]","described","_dtc_ICrmCompensatorVariants_Interface","comsvcs/ICrmCompensatorVariants","cos.icrmcompensatorvariants"]
old-location: cos\icrmcompensatorvariants.htm
tech.root: cos
ms.assetid: 44b80062-b2bb-4c34-b9e1-31229c8e40ca
ms.date: 12/05/2018
ms.keywords: ICrmCompensatorVariants, ICrmCompensatorVariants interface [COM+], ICrmCompensatorVariants interface [COM+],described, _dtc_ICrmCompensatorVariants_Interface, comsvcs/ICrmCompensatorVariants, cos.icrmcompensatorvariants
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
 - ICrmCompensatorVariants
 - comsvcs/ICrmCompensatorVariants
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
 - ICrmCompensatorVariants
---

# ICrmCompensatorVariants interface


## -description

Delivers structured log records to the CRM Compensator when using Microsoft Visual Basic.

## -inheritance

The <b>ICrmCompensatorVariants</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICrmCompensatorVariants</b> also has these types of members:

## -remarks

The CRM clerk determines the CLSID of the CRM Compensator using the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmlogcontrol-registercompensator">ICrmLogControl::RegisterCompensator</a> method. It next calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> specifying the CLSID of this CRM Compensator, and then it calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for both the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensator">ICrmCompensator</a> interface and the <b>ICrmCompensatorVariants</b> interface.

## -see-also

<a href="/windows/desktop/cossdk/com--compensating-resource-manager">COM+ Compensating Resource Manager</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensator">ICrmCompensator</a>
