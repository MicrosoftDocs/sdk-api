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

# IWbemDecoupledBasicEventProvider::GetService


## -description


The 
<b>IWbemDecoupledBasicEventProvider::GetService</b> method retrieves an <b>IWbemService</b> object to be used to call back into WMI. This method provides for fully concurrent access.


## -parameters




### -param a_Flags




### -param a_Context




### -param a_Service






#### - lFlags [in]

Reserved for future use.


#### - pContext [in]

Reserved for future use.


#### - pService [out]

Pointer to an <b>IWbemService</b> object that can be used to retrieve information from WMI.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.



