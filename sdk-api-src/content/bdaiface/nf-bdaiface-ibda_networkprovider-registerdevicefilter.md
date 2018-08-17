---
UID: NF:bdaiface.IBDA_NetworkProvider.RegisterDeviceFilter
title: IBDA_NetworkProvider::RegisterDeviceFilter
author: windows-sdk-content
description: The RegisterDeviceFilter method is called by a BDA device filter to register itself in the filter graph.
old-location: mstv\ibda_networkprovider_registerdevicefilter.htm
old-project: mstv
ms.assetid: 88050024-5960-4ce5-8645-82db3e17b12c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_NetworkProvider interface [Microsoft TV Technologies],RegisterDeviceFilter method, IBDA_NetworkProvider.RegisterDeviceFilter, IBDA_NetworkProvider::RegisterDeviceFilter, IBDA_NetworkProviderRegisterDeviceFilter, RegisterDeviceFilter, RegisterDeviceFilter method [Microsoft TV Technologies], RegisterDeviceFilter method [Microsoft TV Technologies],IBDA_NetworkProvider interface, bdaiface/IBDA_NetworkProvider::RegisterDeviceFilter, mstv.ibda_networkprovider_registerdevicefilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.redist: 
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
 - IBDA_NetworkProvider.RegisterDeviceFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_NetworkProvider::RegisterDeviceFilter


## -description



The <b>RegisterDeviceFilter</b> method is called by a BDA device filter to register itself in the filter graph.




## -parameters




### -param pUnkFilterControl [in]

Pointer to the filter's <b>IUnknown</b> interface.


### -param ppvRegisitrationContext






#### - pulRegisitrationContext [out]

Pointer that receives the registration context. The filter should store this value and return it in the call to <b>UnRegisterDeviceFilter</b>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693410(v=VS.85).aspx">IBDA_NetworkProvider Interface</a>
 

 

