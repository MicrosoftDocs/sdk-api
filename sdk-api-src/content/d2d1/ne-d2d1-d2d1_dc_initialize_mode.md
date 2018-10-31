---
UID: NE:d2d1.D2D1_DC_INITIALIZE_MODE
title: D2D1_DC_INITIALIZE_MODE
author: windows-sdk-content
description: Specifies how a device context is initialized for GDI rendering when it is retrieved from the render target.
old-location: direct2d\D2D1_DC_INITIALIZE_MODE.htm
tech.root: direct2d
ms.assetid: a7837fe4-6e11-42a0-8a85-cba42e0f123a
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: D2D1_DC_INITIALIZE_MODE, D2D1_DC_INITIALIZE_MODE enumeration [Direct2D], D2D1_DC_INITIALIZE_MODE_CLEAR, D2D1_DC_INITIALIZE_MODE_COPY, d2d1/D2D1_DC_INITIALIZE_MODE, d2d1/D2D1_DC_INITIALIZE_MODE_CLEAR, d2d1/D2D1_DC_INITIALIZE_MODE_COPY, direct2d.D2D1_DC_INITIALIZE_MODE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_DC_INITIALIZE_MODE
product: Windows
targetos: Windows
req.typenames: D2D1_DC_INITIALIZE_MODE
req.redist: 
---

# D2D1_DC_INITIALIZE_MODE enumeration


## -description


 Specifies how a device context is initialized for GDI rendering when it is retrieved from the render target.


## -enum-fields




### -field D2D1_DC_INITIALIZE_MODE_COPY

The current contents of the render target are copied to the device context when it is initialized. 


### -field D2D1_DC_INITIALIZE_MODE_CLEAR

The device context is cleared to transparent black when it is initialized.


### -field D2D1_DC_INITIALIZE_MODE_FORCE_DWORD




## -remarks



Use this enumeration with the <a href="https://msdn.microsoft.com/40797258-84a0-44ee-8b64-04ceb3eb1998">ID2D1GdiInteropRenderTarget::GetDC</a> method to specify how the device context is  initialized for GDI rendering.




## -see-also




<a href="https://msdn.microsoft.com/40797258-84a0-44ee-8b64-04ceb3eb1998">ID2D1GdiInteropRenderTarget::GetDC</a>
 

 

