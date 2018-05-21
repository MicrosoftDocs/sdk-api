---
UID: NF:uxtheme.GetThemePropertyOrigin
title: GetThemePropertyOrigin function
author: windows-driver-content
description: Retrieves the location of the theme property definition for a property.
old-location: controls\GetThemePropertyOrigin.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemepropertyorigin.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
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
req.typenames: BP_BUFFERFORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	UxTheme.dll
api_name:
-	GetThemePropertyOrigin
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# GetThemePropertyOrigin function


## -description


Retrieves the location of the theme property definition for a property. 


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/3c496a3f-e4d0-4938-af66-85df93829cd8">OpenThemeData</a> to create an HTHEME.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the theme. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param iPropId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the property to retrieve. You may use any of the property values from Vssym32.h. These values are described in the reference pages for the functions that use them. For instance, the <a href="https://msdn.microsoft.com/f217ccbd-bbce-4ac3-a723-873011fa12c4">GetThemeInt</a> function uses the TMT_BORDERSIZE value. See the <a href="https://msdn.microsoft.com/f1d01045-a296-4b39-bd42-1262ba4ad3d2">Visual Styles Reference</a> for a list of functions.


### -param pOrigin [out]

Type: <b><a href="https://msdn.microsoft.com/245a7051-ac29-41e3-884a-4f568f02bff4">PROPERTYORIGIN</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/245a7051-ac29-41e3-884a-4f568f02bff4">PROPERTYORIGIN</a> enumerated type that indicates where the property was or was not found.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b0e22022-fea9-43d1-8ef0-7a1c518760f1">Property Identifiers</a>
 

 

