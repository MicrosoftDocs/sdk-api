---
UID: NF:ddraw.IDirectDrawClipper.SetHWnd
title: IDirectDrawClipper::SetHWnd (ddraw.h)
description: Sets the window handle that the clipper object uses to obtain clipping information.
helpviewer_keywords: ["IDirectDrawClipper interface [DirectDraw]","SetHWnd method","IDirectDrawClipper.SetHWnd","IDirectDrawClipper::SetHWnd","SetHWnd","SetHWnd method [DirectDraw]","SetHWnd method [DirectDraw]","IDirectDrawClipper interface","ddraw/IDirectDrawClipper::SetHWnd","directdraw.idirectdrawclipper_sethwnd"]
old-location: directdraw\idirectdrawclipper_sethwnd.htm
tech.root: directdraw
ms.assetid: 7683bccd-3f5c-4098-9041-9c66853cda0e
ms.date: 12/05/2018
ms.keywords: IDirectDrawClipper interface [DirectDraw],SetHWnd method, IDirectDrawClipper.SetHWnd, IDirectDrawClipper::SetHWnd, SetHWnd, SetHWnd method [DirectDraw], SetHWnd method [DirectDraw],IDirectDrawClipper interface, ddraw/IDirectDrawClipper::SetHWnd, directdraw.idirectdrawclipper_sethwnd
f1_keywords:
- ddraw/IDirectDrawClipper.SetHWnd
dev_langs:
- c++
req.header: ddraw.h
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ddraw.dll
api_name:
- IDirectDrawClipper.SetHWnd
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawClipper::SetHWnd


## -description


Sets the window handle that the clipper object uses to obtain clipping information.


## -parameters




### -param arg1 [in]

Currently not used and must be set to 0.


### -param arg2 [in]

Window handle that obtains the clipping information.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDCLIPLIST</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>



## -remarks



You must use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access the  <b>SetHWnd</b> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nn-ddraw-idirectdrawclipper">IDirectDrawClipper</a>
 

 

