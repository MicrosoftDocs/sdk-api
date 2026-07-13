---
UID: NN:mfidl.IMFSignedLibrary
title: IMFSignedLibrary (mfidl.h)
description: Provides a method that allows content protection systems to get the procedure address of a function in the signed library. This method provides the same functionality as GetProcAddress which is not available to Windows Store apps.
helpviewer_keywords: ["IMFSignedLibrary","IMFSignedLibrary interface [Media Foundation]","IMFSignedLibrary interface [Media Foundation]","described","mf.imfsignedlibrary","mfidl/IMFSignedLibrary"]
old-location: mf\imfsignedlibrary.htm
tech.root: mf
ms.assetid: 1170fd74-7da4-49a8-b095-dd1572db382d
ms.date: 12/05/2018
ms.keywords: IMFSignedLibrary, IMFSignedLibrary interface [Media Foundation], IMFSignedLibrary interface [Media Foundation],described, mf.imfsignedlibrary, mfidl/IMFSignedLibrary
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
 - IMFSignedLibrary
 - mfidl/IMFSignedLibrary
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
 - IMFSignedLibrary
---

# IMFSignedLibrary interface


## -description

Provides a method that allows content protection systems to get the procedure address of a function in the signed library.  This method provides the same functionality as <b>GetProcAddress</b> which is not available to Windows Store apps.

## -inheritance

The <b>IMFSignedLibrary</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSignedLibrary</b> also has these types of members:

## -remarks

See  <a href="/windows/desktop/api/mfidl/nf-mfidl-mfloadsignedlibrary">MFLoadSignedLibrary</a> for an example of how to create and use an <b>IMFSignedLibrary</b> object.

## -see-also

<a href="/windows/desktop/api/mfidl/nf-mfidl-mfloadsignedlibrary">MFLoadSignedLibrary</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
