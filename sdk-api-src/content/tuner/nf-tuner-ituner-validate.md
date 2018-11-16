---
UID: NF:tuner.ITuner.Validate
title: ITuner::Validate
author: windows-sdk-content
description: The Validate method returns a value indicating that the tune request can be carried out.
old-location: mstv\ituner_validate.htm
tech.root: mstv
ms.assetid: 10b238b1-1c71-4104-8c2d-f8446f0a3466
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITuner interface [Microsoft TV Technologies],Validate method, ITuner.Validate, ITuner::Validate, ITunerValidate, Validate, Validate method [Microsoft TV Technologies], Validate method [Microsoft TV Technologies],ITuner interface, mstv.ituner_validate, tuner/ITuner::Validate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - ITuner.Validate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tuner.h
: 
- ITuner.Validate
: 
---

# ITuner::Validate


## -description



The <b>Validate</b> method returns a value indicating that the tune request can be carried out.




## -parameters




### -param TuneRequest [in]

Pointer to the tune request object.


## -returns



When the method is successful, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The Network Provider will first query for its preferred tune request interface(s). If any are found, the Network Provider will validate that the tune request could be carried out. If none are available, it will then query for its preferred tuning space interface(s). If any are found, the Network Provider will validate that it could configure itself for the given tuning space.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1bc965a5-6bc9-488a-a2f9-f35d0cfbcccd">ITuner Interface</a>
 

 

