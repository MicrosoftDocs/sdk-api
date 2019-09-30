---
UID: NF:dcomp.IDCompositionDesktopDevice.CreateSurfaceFromHandle
title: IDCompositionDesktopDevice::CreateSurfaceFromHandle (dcomp.h)
author: windows-sdk-content
description: Creates a new composition surface object that wraps an existing composition surface.
old-location: directcomp\idcompositiondesktopdevice_createsurfacefromhandle.htm
tech.root: directcomp
ms.assetid: BB0F8F27-16D8-42EB-874B-C16E8511B0B5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateSurfaceFromHandle, CreateSurfaceFromHandle method [DirectComposition], CreateSurfaceFromHandle method [DirectComposition],IDCompositionDesktopDevice interface, IDCompositionDesktopDevice interface [DirectComposition],CreateSurfaceFromHandle method, IDCompositionDesktopDevice.CreateSurfaceFromHandle, IDCompositionDesktopDevice::CreateSurfaceFromHandle, dcomp/IDCompositionDesktopDevice::CreateSurfaceFromHandle, directcomp.idcompositiondesktopdevice_createsurfacefromhandle
ms.topic: method
f1_keywords: 
 - "dcomp/IDCompositionDesktopDevice.CreateSurfaceFromHandle"
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - dcomp.h
api_name:
 - IDCompositionDesktopDevice.CreateSurfaceFromHandle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionDesktopDevice::CreateSurfaceFromHandle


## -description


Creates a new composition surface object that wraps an existing composition surface.


## -parameters




### -param handle [in]

The handle of an existing composition surface that was created by a call to the <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle">DCompositionCreateSurfaceHandle</a> function.



### -param surface [out]

The new composition surface object. This parameter must not be NULL.



## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondesktopdevice">IDCompositionDesktopDevice</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-setcontent">IDCompositionVisual::SetContent</a>
 

 

