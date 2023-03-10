---
UID: NF:comsvcs.ICrmCompensator.EndAbort
title: ICrmCompensator::EndAbort (comsvcs.h)
description: Notifies the CRM Compensator that it has received all the log records available during the abort phase. (ICrmCompensator.EndAbort)
helpviewer_keywords: ["EndAbort","EndAbort method [COM+]","EndAbort method [COM+]","ICrmCompensator interface","ICrmCompensator interface [COM+]","EndAbort method","ICrmCompensator.EndAbort","ICrmCompensator::EndAbort","_dtc_ICrmCompensator_EndAbort","comsvcs/ICrmCompensator::EndAbort","cos.icrmcompensator_endabort"]
old-location: cos\icrmcompensator_endabort.htm
tech.root: cos
ms.assetid: 009209fe-0910-4db1-b5c2-accd7239c3e5
ms.date: 12/05/2018
ms.keywords: EndAbort, EndAbort method [COM+], EndAbort method [COM+],ICrmCompensator interface, ICrmCompensator interface [COM+],EndAbort method, ICrmCompensator.EndAbort, ICrmCompensator::EndAbort, _dtc_ICrmCompensator_EndAbort, comsvcs/ICrmCompensator::EndAbort, cos.icrmcompensator_endabort
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
 - ICrmCompensator::EndAbort
 - comsvcs/ICrmCompensator::EndAbort
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
 - ICrmCompensator.EndAbort
---

# ICrmCompensator::EndAbort


## -description

Notifies the CRM Compensator that it has received all the log records available during the abort phase. All log records for this transaction can be discarded from the log after this method has completed.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensator">ICrmCompensator</a>
