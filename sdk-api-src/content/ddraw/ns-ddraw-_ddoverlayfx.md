---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _DDOVERLAYFX structure


## -description


The <b>DDOVERLAYFX</b> structure passes overlay information to the <a href="https://msdn.microsoft.com/8706c6ca-cd17-490a-8ff9-9470a7d7a150">IDirectDrawSurface7::UpdateOverlay</a> method.




## -struct-fields




### -field dwSize

Size of the structure, in bytes. This member must be initialized before the structure is used.


### -field dwAlphaEdgeBlendBitDepth

Bit depth used to specify the constant for an alpha edge blend.


### -field dwAlphaEdgeBlend

Constant to use as the alpha for an edge blend.


### -field dwReserved

Reserved


### -field dwAlphaDestConstBitDepth

Bit depth used to specify the alpha constant for a destination.


### -field DUMMYUNIONNAMEN.dwAlphaDestConst

 


### -field DUMMYUNIONNAMEN.lpDDSAlphaDest

 


### -field dwAlphaSrcConstBitDepth

Bit depth used to specify the alpha constant for a source.


### -field DUMMYUNIONNAMEN

 


### -field DUMMYUNIONNAMEN.dwAlphaSrcConst

 


### -field DUMMYUNIONNAMEN.lpDDSAlphaSrc

 


### -field dckDestColorkey

Destination color key for the overlay.


### -field dckSrcColorkey

Source color key for the overlay.


### -field dwDDFX

The following flags that specify overlay effects:



#### DDOVERFX_ARITHSTRETCHY

If stretching, use arithmetic stretching along the y-axis for this overlay.



#### DDOVERFX_MIRRORLEFTRIGHT

Mirror the overlay around the vertical axis.



#### DDOVERFX_MIRRORUPDOWN

Mirror the overlay around the horizontal axis.


### -field dwFlags

Currently not used and must be set to 0.


#### - DUMMYUNIONNAMEN(1)



#### dwAlphaDestConst

Constant to use as the alpha channel for a destination.



#### lpDDSAlphaDest

Address of a surface to use as the alpha channel for a destination.


#### - DUMMYUNIONNAMEN(2)



#### dwAlphaSrcConst

Constant to use as the alpha channel for a source.



#### lpDDSAlphaSrc

Address of a surface to use as the alpha channel for a source.


## -remarks



The unions in this structure have been updated to work with compilers that do not support nameless unions. If your compiler does not support nameless unions, define the NONAMELESSUNION token before including the Ddraw.h header file.





