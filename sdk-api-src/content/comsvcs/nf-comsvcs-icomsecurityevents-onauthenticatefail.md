---
UID: NF:comsvcs.IComSecurityEvents.OnAuthenticateFail
title: IComSecurityEvents::OnAuthenticateFail (comsvcs.h)
author: windows-sdk-content
description: Generated when a method call level authentication fails.
old-location: cos\icomsecurityevents_onauthenticatefail.htm
tech.root: cossdk
ms.assetid: 3ead4865-924c-40fb-9ed8-5b98c603c5cf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComSecurityEvents interface [COM+],OnAuthenticateFail method, IComSecurityEvents.OnAuthenticateFail, IComSecurityEvents::OnAuthenticateFail, OnAuthenticateFail, OnAuthenticateFail method [COM+], OnAuthenticateFail method [COM+],IComSecurityEvents interface, _dtc_IComSecurityEvents_OnAuthenticateFail, comsvcs/IComSecurityEvents::OnAuthenticateFail, cos.icomsecurityevents_onauthenticatefail
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
 - IComSecurityEvents.OnAuthenticateFail
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComSecurityEvents::OnAuthenticateFail


## -description


Generated when a method call level authentication fails.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms688276(v=VS.85).aspx">COMSVCSEVENTINFO</a> structure.


### -param guidActivity [in]

The identifier of the activity in which the object is created.


### -param ObjectID [in]

 The just-in-time activated object.


### -param guidIID [in]

The IID of the method.


### -param iMeth [in]

The v-table index of the method.


### -param cbByteOrig [in]

The number of bytes in the security identifier for the original caller.


### -param pSidOriginalUser [in]

The security identifier for the original caller.


### -param cbByteCur [in]

The number of bytes in the security identifier for the current caller.


### -param pSidCurrentUser [in]

The security identifier for the current caller.


### -param bCurrentUserInpersonatingInProc [in]

Indicates whether the current user is impersonating.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/83366f18-8dd4-4c3d-8362-4fbcc4c33b95">IComSecurityEvents</a>
 

 

