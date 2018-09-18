---
UID: NF:gdipluseffects.Levels.GetParameters
title: Levels::GetParameters
author: windows-sdk-content
description: The Levels::GetParameters method gets the current values of the parameters of this Levels object.
old-location: gdiplus\_gdiplus_CLASS_Levels_GetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\levelsclass\levelsmethods\getparameters.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],Levels class, Levels class [GDI+],GetParameters method, Levels.GetParameters, Levels::GetParameters, _gdiplus_CLASS_Levels_GetParameters_, gdiplus._gdiplus_CLASS_Levels_GetParameters_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluseffects.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Levels.GetParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# Levels::GetParameters


## -description


The <b>Levels::GetParameters</b> method gets the current values of the parameters of this <a href="https://msdn.microsoft.com/0256fa03-f029-472e-988a-9eb7ed117673">Levels</a> object.


## -parameters




### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size, in bytes, of a <a href="https://msdn.microsoft.com/84f6009b-ac6c-42e5-b151-9189e09c053d">LevelsParams</a> structure.


### -param parameters [out]

Type: <b><a href="https://msdn.microsoft.com/84f6009b-ac6c-42e5-b151-9189e09c053d">LevelsParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/84f6009b-ac6c-42e5-b151-9189e09c053d">LevelsParams</a> structure that receives the parameter values.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/0256fa03-f029-472e-988a-9eb7ed117673">Levels</a>



<a href="https://msdn.microsoft.com/928f88d3-1fc0-49a5-b286-794c157d10aa">Levels::SetParameters</a>
 

 

