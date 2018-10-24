---
UID: NF:uxtheme.GetThemePropertyOrigin
title: GetThemePropertyOrigin function
author: windows-sdk-content
description: Retrieves the location of the theme property definition for a property.
old-location: controls\GetThemePropertyOrigin.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemepropertyorigin.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetThemePropertyOrigin, GetThemePropertyOrigin function [Windows Controls], controls.GetThemePropertyOrigin, controls.inet_GetThemePropertyOrigin, inet_GetThemePropertyOrigin, inet_GetThemePropertyOrigin_cpp, uxtheme/GetThemePropertyOrigin
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - GetThemePropertyOrigin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetThemePropertyOrigin function


## -description


Retrieves the location of the theme property definition for a property. 


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/en-us/library/Bb759821(v=VS.85).aspx">OpenThemeData</a> to create an HTHEME.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the theme. See <a href="https://msdn.microsoft.com/en-us/library/Bb773210(v=VS.85).aspx">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="https://msdn.microsoft.com/en-us/library/Bb773210(v=VS.85).aspx">Parts and States</a>.


### -param iPropId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the property to retrieve. You may use any of the property values from Vssym32.h. These values are described in the reference pages for the functions that use them. For instance, the <a href="https://msdn.microsoft.com/en-us/library/Bb759749(v=VS.85).aspx">GetThemeInt</a> function uses the TMT_BORDERSIZE value. See the <a href="https://msdn.microsoft.com/en-us/library/Bb773178(v=VS.85).aspx">Visual Styles Reference</a> for a list of functions.


### -param arg1

TBD




#### - pOrigin [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb759837(v=VS.85).aspx">PROPERTYORIGIN</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb759837(v=VS.85).aspx">PROPERTYORIGIN</a> enumerated type that indicates where the property was or was not found.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb773213(v=VS.85).aspx">Property Identifiers</a>
 

 

