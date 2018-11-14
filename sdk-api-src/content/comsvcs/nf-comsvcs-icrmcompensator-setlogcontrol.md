---
UID: NF:comsvcs.ICrmCompensator.SetLogControl
title: ICrmCompensator::SetLogControl
author: windows-sdk-content
description: Delivers an ICrmLogControl interface to the CRM Compensator so that it can write further log records during transaction completion.
old-location: cos\icrmcompensator_setlogcontrol.htm
tech.root: cossdk
ms.assetid: a68e49c7-a0d3-4c37-b438-864578e4a680
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICrmCompensator interface [COM+],SetLogControl method, ICrmCompensator.SetLogControl, ICrmCompensator::SetLogControl, SetLogControl, SetLogControl method [COM+], SetLogControl method [COM+],ICrmCompensator interface, _dtc_ICrmCompensator_SetLogControl, comsvcs/ICrmCompensator::SetLogControl, cos.icrmcompensator_setlogcontrol
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
 - ICrmCompensator.SetLogControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- ICrmCompensator.SetLogControl
: 
---

# ICrmCompensator::SetLogControl


## -description


Delivers an <a href="https://msdn.microsoft.com/3309ed58-8161-46f3-93bc-afc0c9bc8d50">ICrmLogControl</a> interface to the CRM Compensator so that it can write further log records during transaction completion. This method is the first method called on the CRM Compensator after it has been created.


## -parameters




### -param pLogControl [in]

A pointer to the <a href="https://msdn.microsoft.com/3309ed58-8161-46f3-93bc-afc0c9bc8d50">ICrmLogControl</a> interface of the CRM clerk.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



CRM Compensator errors cause failfast of the server process, unless this has been specifically overridden (through a registry flag) for this particular CRM Compensator CLSID. See <a href="https://msdn.microsoft.com/c4e68451-fb8a-45b5-9968-7d5a6418dfe8">COM+ CRM Registry Settings</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/9e5a8f2c-4115-42bd-a541-d0ce75c45b72">ICrmCompensator</a>
 

 

