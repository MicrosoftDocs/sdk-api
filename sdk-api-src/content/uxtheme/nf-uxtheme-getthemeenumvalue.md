---
UID: NF:uxtheme.GetThemeEnumValue
title: GetThemeEnumValue function
author: windows-driver-content
description: Retrieves the value of an enumerated type property.
old-location: controls\GetThemeEnumValue.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemeenumvalue.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: GetThemeEnumValue, GetThemeEnumValue function [Windows Controls], controls.GetThemeEnumValue, controls.inet_GetThemeEnumValue, inet_GetThemeEnumValue, inet_GetThemeEnumValue_cpp, uxtheme/GetThemeEnumValue
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
-	Ext-MS-Win-UXTheme-Themes-l1-1-0.dll
-	xamlpalwp.dll
-	ext-ms-win-uxtheme-themes-l1-1-1.dll
api_name:
-	GetThemeEnumValue
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# GetThemeEnumValue function


## -description


Retrieves the value of an enumerated type property.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/3c496a3f-e4d0-4938-af66-85df93829cd8">OpenThemeData</a> to create an HTHEME.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the enumerated type property. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>. 


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param iPropId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the property to retrieve. For a list of possible values, see <a href="https://msdn.microsoft.com/b0e22022-fea9-43d1-8ef0-7a1c518760f1">Property Identifiers</a>.


### -param piVal [out]

Type: <b>int*</b>

Pointer to an <b>int</b> that receives the enumerated type value.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b0e22022-fea9-43d1-8ef0-7a1c518760f1">Property Identifiers</a>
 

 

