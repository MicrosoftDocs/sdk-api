---
UID: NF:comsvcs.IComSecurityEvents.OnAuthenticate
title: IComSecurityEvents::OnAuthenticate (comsvcs.h)
description: Generated when a method call level authentication succeeds.
helpviewer_keywords: ["IComSecurityEvents interface [COM+]","OnAuthenticate method","IComSecurityEvents.OnAuthenticate","IComSecurityEvents::OnAuthenticate","OnAuthenticate","OnAuthenticate method [COM+]","OnAuthenticate method [COM+]","IComSecurityEvents interface","_dtc_IComSecurityEvents_OnAuthenticate","comsvcs/IComSecurityEvents::OnAuthenticate","cos.icomsecurityevents_onauthenticate"]
old-location: cos\icomsecurityevents_onauthenticate.htm
tech.root: cos
ms.assetid: 4be635c6-9601-419d-933e-555b2ae6b73d
ms.date: 12/05/2018
ms.keywords: IComSecurityEvents interface [COM+],OnAuthenticate method, IComSecurityEvents.OnAuthenticate, IComSecurityEvents::OnAuthenticate, OnAuthenticate, OnAuthenticate method [COM+], OnAuthenticate method [COM+],IComSecurityEvents interface, _dtc_IComSecurityEvents_OnAuthenticate, comsvcs/IComSecurityEvents::OnAuthenticate, cos.icomsecurityevents_onauthenticate
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
 - IComSecurityEvents::OnAuthenticate
 - comsvcs/IComSecurityEvents::OnAuthenticate
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
 - IComSecurityEvents.OnAuthenticate
---

# IComSecurityEvents::OnAuthenticate


## -description

Generated when a method call level authentication succeeds. When you set an authentication level for an application, you determine what degree of authentication is performed when clients call into the application.

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