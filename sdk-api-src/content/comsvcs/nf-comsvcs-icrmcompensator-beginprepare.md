---
UID: NF:comsvcs.ICrmCompensator.BeginPrepare
title: ICrmCompensator::BeginPrepare (comsvcs.h)
description: Notifies the CRM Compensator of the prepare phase of the transaction completion and that records are about to be delivered.helpviewer_keywords: ["BeginPrepare","BeginPrepare method [COM+]","BeginPrepare method [COM+]","ICrmCompensator interface","ICrmCompensator interface [COM+]","BeginPrepare method","ICrmCompensator.BeginPrepare","ICrmCompensator::BeginPrepare","_dtc_ICrmCompensator_BeginPrepare","comsvcs/ICrmCompensator::BeginPrepare","cos.icrmcompensator_beginprepare"]
old-location: cos\icrmcompensator_beginprepare.htm
tech.root: cossdk
ms.assetid: 316a9b00-5843-40b3-9c72-a71da21a81d0
ms.date: 12/05/2018
ms.keywords: BeginPrepare, BeginPrepare method [COM+], BeginPrepare method [COM+],ICrmCompensator interface, ICrmCompensator interface [COM+],BeginPrepare method, ICrmCompensator.BeginPrepare, ICrmCompensator::BeginPrepare, _dtc_ICrmCompensator_BeginPrepare, comsvcs/ICrmCompensator::BeginPrepare, cos.icrmcompensator_beginprepare
f1_keywords:
- comsvcs/ICrmCompensator.BeginPrepare
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComSvcs.h
api_name:
- ICrmCompensator.BeginPrepare
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICrmCompensator::BeginPrepare


## -description


Notifies the CRM Compensator of the prepare phase of the transaction completion and that records are about to be delivered. Prepare notifications are never received during recovery, only during normal processing.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensator">ICrmCompensator</a>
 

 

