---
UID: NF:comsvcs.ICrmCompensator.EndPrepare
title: ICrmCompensator::EndPrepare (comsvcs.h)
description: Notifies the CRM Compensator that it has had all the log records available during the prepare phase. (ICrmCompensator.EndPrepare)
helpviewer_keywords: ["EndPrepare","EndPrepare method [COM+]","EndPrepare method [COM+]","ICrmCompensator interface","ICrmCompensator interface [COM+]","EndPrepare method","ICrmCompensator.EndPrepare","ICrmCompensator::EndPrepare","_dtc_ICrmCompensator_EndPrepare","comsvcs/ICrmCompensator::EndPrepare","cos.icrmcompensator_endprepare"]
old-location: cos\icrmcompensator_endprepare.htm
tech.root: cos
ms.assetid: 97dfdd8c-1a33-4173-aa71-cb9c9b1ef5ee
ms.date: 12/05/2018
ms.keywords: EndPrepare, EndPrepare method [COM+], EndPrepare method [COM+],ICrmCompensator interface, ICrmCompensator interface [COM+],EndPrepare method, ICrmCompensator.EndPrepare, ICrmCompensator::EndPrepare, _dtc_ICrmCompensator_EndPrepare, comsvcs/ICrmCompensator::EndPrepare, cos.icrmcompensator_endprepare
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
 - ICrmCompensator::EndPrepare
 - comsvcs/ICrmCompensator::EndPrepare
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
 - ICrmCompensator.EndPrepare
---

# ICrmCompensator::EndPrepare


## -description

Notifies the CRM Compensator that it has had all the log records available during the prepare phase. The CRM Compensator votes on the transaction outcome by using the return parameter of this method.

## -parameters

### -param pfOkToPrepare [out]

Indicates whether the prepare phase succeeded, in which case it is OK to commit this transaction.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensator">ICrmCompensator</a>
