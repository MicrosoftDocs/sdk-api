---
UID: NF:comsvcs.ICrmCompensator.SetLogControl
title: ICrmCompensator::SetLogControl (comsvcs.h)
description: Delivers an ICrmLogControl interface to the CRM Compensator so that it can write further log records during transaction completion.
helpviewer_keywords: ["ICrmCompensator interface [COM+]","SetLogControl method","ICrmCompensator.SetLogControl","ICrmCompensator::SetLogControl","SetLogControl","SetLogControl method [COM+]","SetLogControl method [COM+]","ICrmCompensator interface","_dtc_ICrmCompensator_SetLogControl","comsvcs/ICrmCompensator::SetLogControl","cos.icrmcompensator_setlogcontrol"]
old-location: cos\icrmcompensator_setlogcontrol.htm
tech.root: cos
ms.assetid: a68e49c7-a0d3-4c37-b438-864578e4a680
ms.date: 12/05/2018
ms.keywords: ICrmCompensator interface [COM+],SetLogControl method, ICrmCompensator.SetLogControl, ICrmCompensator::SetLogControl, SetLogControl, SetLogControl method [COM+], SetLogControl method [COM+],ICrmCompensator interface, _dtc_ICrmCompensator_SetLogControl, comsvcs/ICrmCompensator::SetLogControl, cos.icrmcompensator_setlogcontrol
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
 - ICrmCompensator::SetLogControl
 - comsvcs/ICrmCompensator::SetLogControl
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
 - ICrmCompensator.SetLogControl
---

# ICrmCompensator::SetLogControl


## -description

Delivers an <a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmlogcontrol">ICrmLogControl</a> interface to the CRM Compensator so that it can write further log records during transaction completion. This method is the first method called on the CRM Compensator after it has been created.

## -parameters

### -param pLogControl [in]

A pointer to the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmlogcontrol">ICrmLogControl</a> interface of the CRM clerk.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

CRM Compensator errors cause failfast of the server process, unless this has been specifically overridden (through a registry flag) for this particular CRM Compensator CLSID. See <a href="/windows/desktop/cossdk/com--crm-registry-settings">COM+ CRM Registry Settings</a> for more information.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensator">ICrmCompensator</a>