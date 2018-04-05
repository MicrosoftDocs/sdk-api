---
UID: NF:comsvcs.ICrmCompensator.BeginPrepare
title: ICrmCompensator::BeginPrepare method
author: windows-driver-content
description: Notifies the CRM Compensator of the prepare phase of the transaction completion and that records are about to be delivered.
old-location: cos\icrmcompensator_beginprepare.htm
old-project: cossdk
ms.assetid: 316a9b00-5843-40b3-9c72-a71da21a81d0
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: BeginPrepare method [COM+], BeginPrepare method [COM+], ICrmCompensator interface, BeginPrepare,ICrmCompensator.BeginPrepare, ICrmCompensator, ICrmCompensator interface [COM+], BeginPrepare method, ICrmCompensator::BeginPrepare, _dtc_ICrmCompensator_BeginPrepare, comsvcs/ICrmCompensator::BeginPrepare, cos.icrmcompensator_beginprepare
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	ICrmCompensator.BeginPrepare
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICrmCompensator::BeginPrepare method


## -description


Notifies the CRM Compensator of the prepare phase of the transaction completion and that records are about to be delivered. Prepare notifications are never received during recovery, only during normal processing.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9e5a8f2c-4115-42bd-a541-d0ce75c45b72">ICrmCompensator</a>
 

 

