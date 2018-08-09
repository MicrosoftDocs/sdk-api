---
UID: NF:comsvcs.ICrmCompensator.EndCommit
title: ICrmCompensator::EndCommit
author: windows-sdk-content
description: Notifies the CRM Compensator that it has delivered all the log records available during the commit phase.
old-location: cos\icrmcompensator_endcommit.htm
old-project: cossdk
ms.assetid: 83701797-c386-4471-91ed-cbe936b1988e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EndCommit, EndCommit method [COM+], EndCommit method [COM+],ICrmCompensator interface, ICrmCompensator interface [COM+],EndCommit method, ICrmCompensator.EndCommit, ICrmCompensator::EndCommit, _dtc_ICrmCompensator_EndCommit, comsvcs/ICrmCompensator::EndCommit, cos.icrmcompensator_endcommit
ms.prod: windows
ms.technology: windows-sdk
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
 - ICrmCompensator.EndCommit
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICrmCompensator::EndCommit


## -description


Notifies the CRM Compensator that it has delivered all the log records available during the commit phase. All log records for this transaction can be discarded from the log after this method has completed.



## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9e5a8f2c-4115-42bd-a541-d0ce75c45b72">ICrmCompensator</a>
 

 

