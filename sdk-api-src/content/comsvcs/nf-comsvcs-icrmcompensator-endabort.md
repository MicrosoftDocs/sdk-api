---
UID: NF:comsvcs.ICrmCompensator.EndAbort
title: ICrmCompensator::EndAbort
author: windows-sdk-content
description: Notifies the CRM Compensator that it has received all the log records available during the abort phase.
old-location: cos\icrmcompensator_endabort.htm
old-project: cossdk
ms.assetid: 009209fe-0910-4db1-b5c2-accd7239c3e5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EndAbort, EndAbort method [COM+], EndAbort method [COM+],ICrmCompensator interface, ICrmCompensator interface [COM+],EndAbort method, ICrmCompensator.EndAbort, ICrmCompensator::EndAbort, _dtc_ICrmCompensator_EndAbort, comsvcs/ICrmCompensator::EndAbort, cos.icrmcompensator_endabort
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmCompensator.EndAbort
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICrmCompensator::EndAbort


## -description


Notifies the CRM Compensator that it has received all the log records available during the abort phase. All log records for this transaction can be discarded from the log after this method has completed.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9e5a8f2c-4115-42bd-a541-d0ce75c45b72">ICrmCompensator</a>
 

 

