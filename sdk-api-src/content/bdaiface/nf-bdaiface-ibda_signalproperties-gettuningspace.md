---
UID: NF:bdaiface.IBDA_SignalProperties.GetTuningSpace
title: IBDA_SignalProperties::GetTuningSpace (bdaiface.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\ibda_signalproperties_gettuningspace.htm
tech.root: mstv
ms.assetid: 03738363-5923-4e26-a0ea-e345b927140c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTuningSpace, GetTuningSpace method [Microsoft TV Technologies], GetTuningSpace method [Microsoft TV Technologies],IBDA_SignalProperties interface, IBDA_SignalProperties interface [Microsoft TV Technologies],GetTuningSpace method, IBDA_SignalProperties.GetTuningSpace, IBDA_SignalProperties::GetTuningSpace, IBDA_SignalPropertiesGetTuningSpace, bdaiface/IBDA_SignalProperties::GetTuningSpace, mstv.ibda_signalproperties_gettuningspace
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdaiface.h
api_name:
 - IBDA_SignalProperties.GetTuningSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_SignalProperties::GetTuningSpace


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetTuningSpace</b> method retrieves the tuning space for the current tuning request.


## -parameters




### -param pguidTuingSpace [in, out]

Pointer to a variable that receives a GUID identifying the tuning space.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-ibda_signalproperties">IBDA_SignalProperties Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalproperties-puttuningspace">PutTuningSpace</a>
 

 

