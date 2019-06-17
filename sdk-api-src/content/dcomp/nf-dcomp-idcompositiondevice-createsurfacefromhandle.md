---
UID: NF:dcomp.IDCompositionDevice.CreateSurfaceFromHandle
title: IDCompositionDevice::CreateSurfaceFromHandle (dcomp.h)
author: windows-sdk-content
description: Creates a new composition surface object that wraps an existing composition surface.
old-location: directcomp\idcompositiondevice_createsurfacefromhandle.htm
tech.root: directcomp
ms.assetid: 391E98B4-9FFB-4065-91A4-99306B2FEB8F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateSurfaceFromHandle, CreateSurfaceFromHandle method [DirectComposition], CreateSurfaceFromHandle method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateSurfaceFromHandle method, IDCompositionDevice.CreateSurfaceFromHandle, IDCompositionDevice::CreateSurfaceFromHandle, dcomp/IDCompositionDevice::CreateSurfaceFromHandle, directcomp.idcompositiondevice_createsurfacefromhandle
ms.topic: method
f1_keywords: ["dcomp/IDCompositionDevice.CreateSurfaceFromHandle"]
req.header: dcomp.h
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
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDevice.CreateSurfaceFromHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionDevice::CreateSurfaceFromHandle


## -description


Creates a new composition surface object that wraps an existing composition surface.


## -parameters




### -param handle [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HANDLE</a></b>

The handle of an existing composition surface that was created by a call to the <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle">DCompositionCreateSurfaceHandle</a> function.


### -param surface [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionsurface">IUnknown</a>**</b>

The new composition surface object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method enables an application to use a shared composition surface in a composition tree. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createsurface">IDCompositionDevice::CreateSurface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createsurfacefromhwnd">IDCompositionDevice::CreateSurfaceFromHwnd</a>
 

 

