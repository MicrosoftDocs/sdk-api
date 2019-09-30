---
UID: NF:comsvcs.IComExceptionEvents.OnExceptionUser
title: IComExceptionEvents::OnExceptionUser (comsvcs.h)
author: windows-sdk-content
description: Generated for transactional components when an unhandled exception occurs in the user's code.
old-location: cos\icomexceptionevents_onexceptionuser.htm
tech.root: cossdk
ms.assetid: 961e3668-a35e-4e65-8477-fd7457ecc6ca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComExceptionEvents interface [COM+],OnExceptionUser method, IComExceptionEvents.OnExceptionUser, IComExceptionEvents::OnExceptionUser, OnExceptionUser, OnExceptionUser method [COM+], OnExceptionUser method [COM+],IComExceptionEvents interface, _dtc_IComExceptionEvents_OnExceptionUser, comsvcs/IComExceptionEvents::OnExceptionUser, cos.icomexceptionevents_onexceptionuser
ms.topic: method
f1_keywords: 
 - "comsvcs/IComExceptionEvents.OnExceptionUser"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComExceptionEvents.OnExceptionUser
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComExceptionEvents::OnExceptionUser


## -description


Generated for transactional components when an unhandled exception occurs in the user's code.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.


### -param code [in]

The exception code.


### -param address [in]

The address of the exception.


### -param pszStackTrace [in]

The stack trace.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icomexceptionevents">IComExceptionEvents</a>
 

 

