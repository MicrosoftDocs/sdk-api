---
UID: NF:tuner.ILocator.get_Modulation
title: ILocator::get_Modulation (tuner.h)
author: windows-sdk-content
description: The get_Modulation method gets the modulation type.
old-location: mstv\ilocator_get_modulation.htm
tech.root: mstv
ms.assetid: 6aca60fa-ea8d-440d-a037-20537c25a105
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ILocator interface [Microsoft TV Technologies],get_Modulation method, ILocator.get_Modulation, ILocator::get_Modulation, ILocatorget_Modulation, get_Modulation, get_Modulation method [Microsoft TV Technologies], get_Modulation method [Microsoft TV Technologies],ILocator interface, mstv.ilocator_get_modulation, tuner/ILocator::get_Modulation
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
 - ILocator.get_Modulation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILocator::get_Modulation


## -description



The <b>get_Modulation</b> method gets the modulation type.




## -parameters




### -param Modulation [out]

Receives the modulation type, as a member of the <a href="https://msdn.microsoft.com/fd8691d3-a862-4294-8b0b-9723a080d722">ModulationType</a> enumeration.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



See <a href="https://msdn.microsoft.com/84a5b2ce-d26b-4ffc-b757-a799658f2b34">put_Modulation</a> for the definition of <b>ModulationType</b>.




## -see-also




<a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator Interface</a>
 

 

