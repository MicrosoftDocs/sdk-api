---
UID: NF:gdipluseffects.ColorBalance.SetParameters
title: ColorBalance::SetParameters (gdipluseffects.h)
author: windows-sdk-content
description: The ColorBalance::SetParameters method sets the parameters of this ColorBalance object.
old-location: gdiplus\_gdiplus_CLASS_ColorBalance_SetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorbalanceclass\colorbalancemethods\setparameters.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ColorBalance class [GDI+],SetParameters method, ColorBalance.SetParameters, ColorBalance::SetParameters, SetParameters, SetParameters method [GDI+], SetParameters method [GDI+],ColorBalance class, _gdiplus_CLASS_ColorBalance_SetParameters_, gdiplus._gdiplus_CLASS_ColorBalance_SetParameters_
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
 - ColorBalance.SetParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
---

# ColorBalance::SetParameters


## -description


The <b>ColorBalance::SetParameters</b> method sets the parameters of this <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colorbalance">ColorBalance</a> object.


## -parameters




### -param parameters [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/ns-gdipluseffects-colorbalanceparams">ColorBalanceParams</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/ns-gdipluseffects-colorbalanceparams">ColorBalanceParams</a> structure that specifies the parameters.


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colorbalance">ColorBalance</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-colorbalance-getparameters">ColorBalance::GetParameters</a>
 

 

