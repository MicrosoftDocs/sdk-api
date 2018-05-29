---
UID: NF:comsvcs.IComExceptionEvents.OnExceptionUser
title: IComExceptionEvents::OnExceptionUser
author: windows-sdk-content
description: Generated for transactional components when an unhandled exception occurs in the user's code.
old-location: cos\icomexceptionevents_onexceptionuser.htm
old-project: cossdk
ms.assetid: 961e3668-a35e-4e65-8477-fd7457ecc6ca
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IComExceptionEvents interface [COM+],OnExceptionUser method, IComExceptionEvents.OnExceptionUser, IComExceptionEvents::OnExceptionUser, OnExceptionUser, OnExceptionUser method [COM+], OnExceptionUser method [COM+],IComExceptionEvents interface, _dtc_IComExceptionEvents_OnExceptionUser, comsvcs/IComExceptionEvents::OnExceptionUser, cos.icomexceptionevents_onexceptionuser
ms.prod: windows
ms.technology: windows-sdk
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
-	IComExceptionEvents.OnExceptionUser
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComExceptionEvents::OnExceptionUser


## -description


Generated for transactional components when an unhandled exception occurs in the user's code.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param code [in]

The exception code.


### -param address [in]

The address of the exception.


### -param pszStackTrace [in]

The stack trace.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/e484cad0-3b7e-4822-bbde-c953cb0301ca">IComExceptionEvents</a>
 

 

