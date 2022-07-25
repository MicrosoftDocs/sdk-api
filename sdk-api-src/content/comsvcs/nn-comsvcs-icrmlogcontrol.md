---
UID: NN:comsvcs.ICrmLogControl
title: ICrmLogControl (comsvcs.h)
description: Is the means by which the CRM Worker and CRM Compensator write records to the log and make them durable.
helpviewer_keywords: ["ICrmLogControl","ICrmLogControl interface [COM+]","ICrmLogControl interface [COM+]","described","_dtc_ICrmLogControl_Interface","comsvcs/ICrmLogControl","cos.icrmlogcontrol"]
old-location: cos\icrmlogcontrol.htm
tech.root: cos
ms.assetid: 3309ed58-8161-46f3-93bc-afc0c9bc8d50
ms.date: 12/05/2018
ms.keywords: ICrmLogControl, ICrmLogControl interface [COM+], ICrmLogControl interface [COM+],described, _dtc_ICrmLogControl_Interface, comsvcs/ICrmLogControl, cos.icrmlogcontrol
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
 - ICrmLogControl
 - comsvcs/ICrmLogControl
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
 - ICrmLogControl
---

# ICrmLogControl interface


## -description

Is the means by which the CRM Worker and CRM Compensator write records to the log and make them durable.

## -inheritance

The <b>ICrmLogControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICrmLogControl</b> also has these types of members:

## -remarks

The CRM Compensator receives this interface after its instantiation using the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensator-setlogcontrol">ICrmCompensator::SetLogControl</a> or the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-setlogcontrolvariants">ICrmCompensatorVariants::SetLogControlVariants</a> method.

In addition to the return values listed for each method, the methods can also return error codes from the Distributed Transaction Coordinator (DTC) or other standard COM error codes.

## -see-also

<a href="/windows/desktop/cossdk/com--compensating-resource-manager">COM+ Compensating Resource Manager</a>
