---
UID: NN:mfidl.IMFNetCrossOriginSupport
title: IMFNetCrossOriginSupport (mfidl.h)
description: Implemented by clients that want to enforce a cross origin policy for HTML5 media downloads.
helpviewer_keywords: ["IMFNetCrossOriginSupport","IMFNetCrossOriginSupport interface [Media Foundation]","IMFNetCrossOriginSupport interface [Media Foundation]","described","mf.imfnetcrossoriginsupport","mfidl/IMFNetCrossOriginSupport"]
old-location: mf\imfnetcrossoriginsupport.htm
tech.root: mf
ms.assetid: 239E5731-4425-46D4-AFEC-F3E59258B1DF
ms.date: 12/05/2018
ms.keywords: IMFNetCrossOriginSupport, IMFNetCrossOriginSupport interface [Media Foundation], IMFNetCrossOriginSupport interface [Media Foundation],described, mf.imfnetcrossoriginsupport, mfidl/IMFNetCrossOriginSupport
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IMFNetCrossOriginSupport
 - mfidl/IMFNetCrossOriginSupport
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
 - IMFNetCrossOriginSupport
---

# IMFNetCrossOriginSupport interface


## -description



Implemented by clients that want to enforce a cross origin policy for HTML5 media downloads.

## -inheritance

The <b>IMFNetCrossOriginSupport</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFNetCrossOriginSupport</b> also has these types of members:

## -remarks

The Media Foundation network code uses these client callbacks to implement and enforce cross origin downloads.
