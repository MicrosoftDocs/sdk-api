---
UID: NF:dcomp.IDCompositionDevice.CreateRectangleClip
title: IDCompositionDevice::CreateRectangleClip (dcomp.h)
description: Creates a clip object that can be used to restrict the rendering of a visual subtree to a rectangular area.
helpviewer_keywords: ["CreateRectangleClip","CreateRectangleClip method [DirectComposition]","CreateRectangleClip method [DirectComposition]","IDCompositionDevice interface","IDCompositionDevice interface [DirectComposition]","CreateRectangleClip method","IDCompositionDevice.CreateRectangleClip","IDCompositionDevice::CreateRectangleClip","dcomp/IDCompositionDevice::CreateRectangleClip","directcomp.idcompositiondevice_createrectangleclip"]
old-location: directcomp\idcompositiondevice_createrectangleclip.htm
tech.root: directcomp
ms.assetid: b937fbf0-b920-413a-a184-ebe08ee893e5
ms.date: 12/05/2018
ms.keywords: CreateRectangleClip, CreateRectangleClip method [DirectComposition], CreateRectangleClip method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateRectangleClip method, IDCompositionDevice.CreateRectangleClip, IDCompositionDevice::CreateRectangleClip, dcomp/IDCompositionDevice::CreateRectangleClip, directcomp.idcompositiondevice_createrectangleclip
f1_keywords:
- dcomp/IDCompositionDevice.CreateRectangleClip
dev_langs:
- c++
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
- IDCompositionDevice.CreateRectangleClip
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionDevice::CreateRectangleClip


## -description


Creates a clip object that can be used to restrict the rendering of  a visual subtree to a rectangular area.


## -parameters




### -param clip [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionrectangleclip">IDCompositionRectangleClip</a>**</b>

The new clip object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A newly created clip object has a static value of <a href="https://msdn.microsoft.com/library/6bs3y5ya(VS.71).aspx">–FLT_MAX</a> for the left and top properties, and a static value of –FLT_MAX for the right and bottom properties, effectively making it a no-op clip object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)">IDCompositionVisual::SetClip</a>
 

 

