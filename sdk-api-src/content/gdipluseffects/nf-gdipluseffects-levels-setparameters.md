---
UID: NF:gdipluseffects.Levels.SetParameters
title: Levels::SetParameters
author: windows-sdk-content
description: The Levels::SetParameters method sets the parameters of this Levels object.
old-location: gdiplus\_gdiplus_CLASS_Levels_SetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\levelsclass\levelsmethods\setparameters.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: Levels class [GDI+],SetParameters method, Levels.SetParameters, Levels::SetParameters, SetParameters, SetParameters method [GDI+], SetParameters method [GDI+],Levels class, _gdiplus_CLASS_Levels_SetParameters_, gdiplus._gdiplus_CLASS_Levels_SetParameters_
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
 - Levels.SetParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# Levels::SetParameters


## -description


The <b>Levels::SetParameters</b> method sets the parameters of this <a href="https://msdn.microsoft.com/0256fa03-f029-472e-988a-9eb7ed117673">Levels</a> object.


## -parameters




### -param parameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/84f6009b-ac6c-42e5-b151-9189e09c053d">LevelsParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/84f6009b-ac6c-42e5-b151-9189e09c053d">LevelsParams</a> structure that specifies the parameters. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/0256fa03-f029-472e-988a-9eb7ed117673">Levels</a>



<a href="https://msdn.microsoft.com/3f2866dd-e51d-4c4d-9729-79f989ca89da">Levels::GetParameters</a>
 

 

