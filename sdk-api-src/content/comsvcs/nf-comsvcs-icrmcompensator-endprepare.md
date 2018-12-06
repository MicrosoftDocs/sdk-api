---
UID: NF:comsvcs.ICrmCompensator.EndPrepare
title: ICrmCompensator::EndPrepare
author: windows-sdk-content
description: Notifies the CRM Compensator that it has had all the log records available during the prepare phase.
old-location: cos\icrmcompensator_endprepare.htm
tech.root: cossdk
ms.assetid: 97dfdd8c-1a33-4173-aa71-cb9c9b1ef5ee
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EndPrepare, EndPrepare method [COM+], EndPrepare method [COM+],ICrmCompensator interface, ICrmCompensator interface [COM+],EndPrepare method, ICrmCompensator.EndPrepare, ICrmCompensator::EndPrepare, _dtc_ICrmCompensator_EndPrepare, comsvcs/ICrmCompensator::EndPrepare, cos.icrmcompensator_endprepare
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
 - ICrmCompensator.EndPrepare
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICrmCompensator::EndPrepare


## -description


Notifies the CRM Compensator that it has had all the log records available during the prepare phase. The CRM Compensator votes on the transaction outcome by using the return parameter of this method.


## -parameters




### -param pfOkToPrepare [out]

Indicates whether the prepare phase succeeded, in which case it is OK to commit this transaction.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9e5a8f2c-4115-42bd-a541-d0ce75c45b72">ICrmCompensator</a>
 

 

