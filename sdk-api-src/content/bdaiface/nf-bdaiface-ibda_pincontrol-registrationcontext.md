---
UID: NF:bdaiface.IBDA_PinControl.RegistrationContext
title: IBDA_PinControl::RegistrationContext
author: windows-sdk-content
description: The RegistrationContext method retrieves the registration context of a particular pin.
old-location: mstv\ibda_pincontrol_registrationcontext.htm
old-project: mstv
ms.assetid: 6e54bb4e-9c65-4f57-ba4a-c5b35ccaae1f
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IBDA_PinControl interface [Microsoft TV Technologies],RegistrationContext method, IBDA_PinControl.RegistrationContext, IBDA_PinControl::RegistrationContext, IBDA_PinControlRegistrationContext, RegistrationContext, RegistrationContext method [Microsoft TV Technologies], RegistrationContext method [Microsoft TV Technologies],IBDA_PinControl interface, bdaiface/IBDA_PinControl::RegistrationContext, mstv.ibda_pincontrol_registrationcontext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_PinControl.RegistrationContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_PinControl::RegistrationContext


## -description



The <b>RegistrationContext</b> method retrieves the registration context of a particular pin.




## -parameters




### -param pulRegistrationCtx [out]

Pointer that receives the registration context.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The registration context uniquely identifies an instance of a particular pin. A Network Provider does not modify this value; it simply retains it in order to keep track of the pins in the graph.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2d318cc4-b3f2-4fb6-b9e3-8ba8312ad2ae">IBDA_PinControl Interface</a>
 

 

