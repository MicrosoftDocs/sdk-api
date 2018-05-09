---
UID: NF:comsvcs.IMtsEvents.get_PackageName
title: IMtsEvents::get_PackageName
author: windows-driver-content
description: Retrieves the name of the package in which the instance of the object that implements the IMtsEvents interface is running.
old-location: cos\imtsevents_get_packagename.htm
old-project: cossdk
ms.assetid: 0b23828f-cadc-472d-9186-0712e0120b60
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: IMtsEvents interface [COM+],get_PackageName method, IMtsEvents.get_PackageName, IMtsEvents::get_PackageName, _dtc_IMtsEvents_PackageName, comsvcs/IMtsEvents::get_PackageName, cos.imtsevents_get_packagename, get_PackageName, get_PackageName method [COM+], get_PackageName method [COM+],IMtsEvents interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IMtsEvents.get_PackageName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMtsEvents::get_PackageName


## -description


Retrieves the name of the package in which the instance of the object that implements the <a href="https://msdn.microsoft.com/7db3a373-00d3-480e-8f8e-7e65a468d5dc">IMtsEvents</a> interface is running.


## -parameters




### -param pVal [out]

A pointer to the package name string.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/7db3a373-00d3-480e-8f8e-7e65a468d5dc">IMtsEvents</a>
 

 

