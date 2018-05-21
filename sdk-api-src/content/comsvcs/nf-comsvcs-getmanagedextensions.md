---
UID: NF:comsvcs.GetManagedExtensions
title: GetManagedExtensions function
author: windows-driver-content
description: Determines whether the installed version of COM+ supports special features provided to manage serviced components (managed objects).
old-location: cos\getmanagedextensions.htm
old-project: cossdk
ms.assetid: cffd18c4-6e37-447b-b749-64793711ea56
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetManagedExtensions, GetManagedExtensions function [COM+], _cos_GetManagedExtensions, comsvcs/GetManagedExtensions, cos.getmanagedextensions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ComSvcs.dll
api_name:
-	GetManagedExtensions
product: Windows
targetos: Windows
req.lib: ComSvcs.lib
req.dll: ComSvcs.dll
req.irql: 
---

# GetManagedExtensions function


## -description


Determines whether the installed version of COM+ supports special features provided to manage serviced components (managed objects).


## -parameters




### -param dwExts [out]

Indicates whether the installed version of COM+ supports managed extensions. A value of 1 indicates that it does, while a value of 0 indicates that it does not.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



Several COM+ services, such as <a href="https://msdn.microsoft.com/47b23cae-d5fc-4788-ab1c-93d6d8ee3f01">COM+ Just-in-Time Activation</a> and <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>, support the <a href="https://msdn.microsoft.com/621ffc7d-186e-451c-8d97-9c8291549f51">IManagedActivationEvents</a> interface. This interface provides additional code for managing serviced components (managed objects). To take advantage of this additional code, the serviced component must support the <a href="https://msdn.microsoft.com/7fa5f76e-df07-41b3-8fb0-62b84a034aa5">IManagedObjectInfo</a> interface. The <b>GetManagedExtensions</b> function allows you to determine the availability of this additional code in the installed version of COM+.




## -see-also




<a href="https://msdn.microsoft.com/621ffc7d-186e-451c-8d97-9c8291549f51">IManagedActivationEvents</a>



<a href="https://msdn.microsoft.com/7fa5f76e-df07-41b3-8fb0-62b84a034aa5">IManagedObjectInfo</a>



<a href="https://msdn.microsoft.com/04853859-5d85-4b88-9e1b-422e3454fd3f">IManagedPooledObj</a>
 

 

