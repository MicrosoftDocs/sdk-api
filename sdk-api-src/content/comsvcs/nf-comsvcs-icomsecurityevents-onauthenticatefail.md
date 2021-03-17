---
UID: NF:comsvcs.IComSecurityEvents.OnAuthenticateFail
title: IComSecurityEvents::OnAuthenticateFail (comsvcs.h)
description: Generated when a method call level authentication fails.
helpviewer_keywords: ["IComSecurityEvents interface [COM+]","OnAuthenticateFail method","IComSecurityEvents.OnAuthenticateFail","IComSecurityEvents::OnAuthenticateFail","OnAuthenticateFail","OnAuthenticateFail method [COM+]","OnAuthenticateFail method [COM+]","IComSecurityEvents interface","_dtc_IComSecurityEvents_OnAuthenticateFail","comsvcs/IComSecurityEvents::OnAuthenticateFail","cos.icomsecurityevents_onauthenticatefail"]
old-location: cos\icomsecurityevents_onauthenticatefail.htm
tech.root: cos
ms.assetid: 3ead4865-924c-40fb-9ed8-5b98c603c5cf
ms.date: 12/05/2018
ms.keywords: IComSecurityEvents interface [COM+],OnAuthenticateFail method, IComSecurityEvents.OnAuthenticateFail, IComSecurityEvents::OnAuthenticateFail, OnAuthenticateFail, OnAuthenticateFail method [COM+], OnAuthenticateFail method [COM+],IComSecurityEvents interface, _dtc_IComSecurityEvents_OnAuthenticateFail, comsvcs/IComSecurityEvents::OnAuthenticateFail, cos.icomsecurityevents_onauthenticatefail
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IComSecurityEvents::OnAuthenticateFail
 - comsvcs/IComSecurityEvents::OnAuthenticateFail
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComSecurityEvents.OnAuthenticateFail
---

# IComSecurityEvents::OnAuthenticateFail


## -description

Generated when a method call level authentication fails.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

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

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomsecurityevents">IComSecurityEvents</a>