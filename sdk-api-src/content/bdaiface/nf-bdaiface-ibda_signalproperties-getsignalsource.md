---
UID: NF:bdaiface.IBDA_SignalProperties.GetSignalSource
title: IBDA_SignalProperties::GetSignalSource
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\ibda_signalproperties_getsignalsource.htm
old-project: mstv
ms.assetid: 929ec042-3f43-468e-944a-919dda3893be
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetSignalSource, GetSignalSource method [Microsoft TV Technologies], GetSignalSource method [Microsoft TV Technologies],IBDA_SignalProperties interface, IBDA_SignalProperties interface [Microsoft TV Technologies],GetSignalSource method, IBDA_SignalProperties.GetSignalSource, IBDA_SignalProperties::GetSignalSource, IBDA_SignalPropertiesGetSignalSource, bdaiface/IBDA_SignalProperties::GetSignalSource, mstv.ibda_signalproperties_getsignalsource
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Bdaiface.h
api_name:
-	IBDA_SignalProperties.GetSignalSource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_SignalProperties::GetSignalSource


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetSignalSource</b> method retrieves the signal source for the current tuning request.


## -parameters




### -param pulSignalSource [in, out]

Receives a value identifying the signal source. The value is an arbitrary identifier set by the network provider. If two tuners share the same signal source, they should have the same identifier.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method returns whatever value was last set by calling <a href="https://msdn.microsoft.com/81cd43b1-97a7-4663-984e-2c20a8315c7e">IBDA_SignalProperties::PutSignalSource</a>.

<div class="alert"><b>Note</b>  The <i>pulSignalSource</i> parameter is marked in the IDL file as [in, out] but is used as an [out] parameter. To preserve binary compatibility with previous versions, it has not been changed.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/fe88b628-7959-4d2f-981f-7de9126146f6">IBDA_SignalProperties Interface</a>



<a href="https://msdn.microsoft.com/81cd43b1-97a7-4663-984e-2c20a8315c7e">PutSignalSource</a>
 

 

