---
UID: NN:mfidl.IMFProtectedEnvironmentAccess
title: IMFProtectedEnvironmentAccess (mfidl.h)
description: Provides a method that allows content protection systems to perform a handshake with the protected environment. This is needed because the CreateFile and DeviceIoControl APIs are not available to Windows Store apps.
helpviewer_keywords: ["IMFProtectedEnvironmentAccess","IMFProtectedEnvironmentAccess interface [Media Foundation]","IMFProtectedEnvironmentAccess interface [Media Foundation]","described","mf.imfprotectedenvironmentaccess","mfidl/IMFProtectedEnvironmentAccess"]
old-location: mf\imfprotectedenvironmentaccess.htm
tech.root: mf
ms.assetid: 2cd93bc9-4a42-4e16-80aa-4ecf5900f5e4
ms.date: 12/05/2018
ms.keywords: IMFProtectedEnvironmentAccess, IMFProtectedEnvironmentAccess interface [Media Foundation], IMFProtectedEnvironmentAccess interface [Media Foundation],described, mf.imfprotectedenvironmentaccess, mfidl/IMFProtectedEnvironmentAccess
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFProtectedEnvironmentAccess
 - mfidl/IMFProtectedEnvironmentAccess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFProtectedEnvironmentAccess
---

# IMFProtectedEnvironmentAccess interface


## -description

Provides a method that allows content protection systems to perform a handshake with the protected environment. This is needed because the <b>CreateFile</b> and <b>DeviceIoControl</b> APIs are not available to Windows Store apps.

## -inheritance

The <b>IMFProtectedEnvironmentAccess</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFProtectedEnvironmentAccess</b> also has these types of members:

## -remarks

See  <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreateprotectedenvironmentaccess">MFCreateProtectedEnvironmentAccess</a> for an example of how to create and use an <b>IMFProtectedEnvironmentAccess</b> object.

## -see-also

<a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreateprotectedenvironmentaccess">MFCreateProtectedEnvironmentAccess</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
