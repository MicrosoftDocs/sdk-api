---
UID: NF:dcomp.IDCompositionDevice.CreateSurfaceFromHandle
title: IDCompositionDevice::CreateSurfaceFromHandle
author: windows-sdk-content
description: Creates a new composition surface object that wraps an existing composition surface.
old-location: directcomp\idcompositiondevice_createsurfacefromhandle.htm
tech.root: directcomp
ms.assetid: 391E98B4-9FFB-4065-91A4-99306B2FEB8F
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateSurfaceFromHandle, CreateSurfaceFromHandle method [DirectComposition], CreateSurfaceFromHandle method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateSurfaceFromHandle method, IDCompositionDevice.CreateSurfaceFromHandle, IDCompositionDevice::CreateSurfaceFromHandle, dcomp/IDCompositionDevice::CreateSurfaceFromHandle, directcomp.idcompositiondevice_createsurfacefromhandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
---

# IDCompositionDevice::CreateSurfaceFromHandle


## -description


Creates a new composition surface object that wraps an existing composition surface.


## -parameters




### -param handle [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HANDLE</a></b>

The handle of an existing composition surface that was created by a call to the <a href="https://msdn.microsoft.com/550BA10B-D582-4A57-A69D-3EFFC7313D8F">DCompositionCreateSurfaceHandle</a> function.


### -param surface [out]

Type: <b><a href="https://msdn.microsoft.com/E271B4DC-5F09-426A-A5D3-43A48F30CB24">IUnknown</a>**</b>

The new composition surface object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method enables an application to use a shared composition surface in a composition tree. 




## -see-also




<a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a>



<a href="https://msdn.microsoft.com/3B321BF8-A7A5-4E40-B548-D88CA45F6DAF">IDCompositionDevice::CreateSurface</a>



<a href="https://msdn.microsoft.com/EA49F8EB-FAC8-421E-854D-C4AA81887EB0">IDCompositionDevice::CreateSurfaceFromHwnd</a>
 

 

