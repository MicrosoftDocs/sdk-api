---
UID: NF:tuner.ITuner.get_TuningSpace
title: ITuner::get_TuningSpace (tuner.h)
author: windows-sdk-content
description: The get_TuningSpace method gets the tuning space currently in effect for the Network Provider.
old-location: mstv\ituner_get_tuningspace.htm
tech.root: mstv
ms.assetid: 01b6a280-d489-4b4f-ae87-17c9b9bb2838
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITuner interface [Microsoft TV Technologies],get_TuningSpace method, ITuner.get_TuningSpace, ITuner::get_TuningSpace, ITunerget_TuningSpace, get_TuningSpace, get_TuningSpace method [Microsoft TV Technologies], get_TuningSpace method [Microsoft TV Technologies],ITuner interface, mstv.ituner_get_tuningspace, tuner/ITuner::get_TuningSpace
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
 - ITuner.get_TuningSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITuner::get_TuningSpace


## -description



The <b>get_TuningSpace</b> method gets the tuning space currently in effect for the Network Provider.




## -parameters




### -param TuningSpace [out]

Address of an <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a> interface pointer that will be set to the current tuning space.


## -returns



When the method is successful, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1bc965a5-6bc9-488a-a2f9-f35d0cfbcccd">ITuner Interface</a>
 

 

