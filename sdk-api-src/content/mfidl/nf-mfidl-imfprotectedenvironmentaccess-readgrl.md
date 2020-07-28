---
UID: NF:mfidl.IMFProtectedEnvironmentAccess.ReadGRL
title: IMFProtectedEnvironmentAccess::ReadGRL (mfidl.h)
description: Gets the Global Revocation List (GLR).
helpviewer_keywords: ["IMFProtectedEnvironmentAccess interface [Media Foundation]","ReadGRL method","IMFProtectedEnvironmentAccess.ReadGRL","IMFProtectedEnvironmentAccess::ReadGRL","ReadGRL","ReadGRL method [Media Foundation]","ReadGRL method [Media Foundation]","IMFProtectedEnvironmentAccess interface","mf.imfprotectedenvironmentaccess_readgrl","mfidl/IMFProtectedEnvironmentAccess::ReadGRL"]
old-location: mf\imfprotectedenvironmentaccess_readgrl.htm
tech.root: mf
ms.assetid: 38b70c99-1823-498c-b3e4-d2cad05278de
ms.date: 12/05/2018
ms.keywords: IMFProtectedEnvironmentAccess interface [Media Foundation],ReadGRL method, IMFProtectedEnvironmentAccess.ReadGRL, IMFProtectedEnvironmentAccess::ReadGRL, ReadGRL, ReadGRL method [Media Foundation], ReadGRL method [Media Foundation],IMFProtectedEnvironmentAccess interface, mf.imfprotectedenvironmentaccess_readgrl, mfidl/IMFProtectedEnvironmentAccess::ReadGRL
f1_keywords:
- mfidl/IMFProtectedEnvironmentAccess.ReadGRL
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- Mfidl.h
api_name:
- IMFProtectedEnvironmentAccess.ReadGRL
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFProtectedEnvironmentAccess::ReadGRL


## -description


Gets the Global Revocation List (GLR).


## -parameters




### -param outputLength

The length of the data returned in <b>output</b>.


### -param output

Receives the contents of the global revocation list file.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Allows reading of the system Global Revocation List (GRL).  




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfprotectedenvironmentaccess">IMFProtectedEnvironmentAccess</a>
 

 

