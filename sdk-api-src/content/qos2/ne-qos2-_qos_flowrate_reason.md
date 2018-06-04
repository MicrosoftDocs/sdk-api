---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _QOS_FLOWRATE_REASON enumeration


## -description


The <b>QOS_FLOWRATE_REASON</b> enumeration indicates the reason for a change in a flow's bandwidth.


## -enum-fields




### -field QOSFlowRateNotApplicable

Indicates that there has not been a change in the flow.


### -field QOSFlowRateContentChange

Indicates that the content of a flow has changed.


### -field QOSFlowRateCongestion

Indicates that the flow has changed due to congestion.


### -field QOSFlowRateHigherContentEncoding


### -field QOSFlowRateUserCaused

Indicates that the user has caused the flow to change.


## -see-also




<a href="https://msdn.microsoft.com/8cae3ba2-beca-45e2-9526-2d917abc2606">QOSQueryFlow</a>



<a href="https://msdn.microsoft.com/022fde13-415e-49aa-8df4-472c4eadd6a0">Quality Windows Audio/Video Experience (qWAVE)</a>
 

 

