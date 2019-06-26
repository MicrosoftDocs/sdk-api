---
UID: NF:ocidl.IOleInPlaceSiteWindowless.CanWindowlessActivate
title: IOleInPlaceSiteWindowless::CanWindowlessActivate (ocidl.h)
author: windows-sdk-content
description: Informs an object if its container can support it as a windowless object that can be in-place activated.
old-location: com\ioleinplacesitewindowless_canwindowlessactivate.htm
tech.root: com
ms.assetid: 8e2f2820-e8d7-4f0e-921d-4fc88feca15f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CanWindowlessActivate, CanWindowlessActivate method [COM], CanWindowlessActivate method [COM],IOleInPlaceSiteWindowless interface, IOleInPlaceSiteWindowless interface [COM],CanWindowlessActivate method, IOleInPlaceSiteWindowless.CanWindowlessActivate, IOleInPlaceSiteWindowless::CanWindowlessActivate, _ole_ioleinplacesitewindowless_canwindowlessactivate, com.ioleinplacesitewindowless_canwindowlessactivate, ocidl/IOleInPlaceSiteWindowless::CanWindowlessActivate
ms.topic: method
f1_keywords: 
 - "ocidl/IOleInPlaceSiteWindowless.CanWindowlessActivate"
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - OCIdl.h
api_name:
 - IOleInPlaceSiteWindowless.CanWindowlessActivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleInPlaceSiteWindowless::CanWindowlessActivate


## -description


Informs an object if its container can support it as a windowless object that can be in-place activated.


## -parameters






## -returns



This method returns S_OK if the object can activate in-place without a window.




## -remarks



If this method returns S_OK, the container can dispatch events to it using <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleinplaceobjectwindowless">IOleInPlaceObjectWindowless</a>.

If this method returns S_FALSE, the object should create a window and behave as a normal compound document object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleinplaceobjectwindowless">IOleInPlaceObjectWindowless</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a>
 

 

