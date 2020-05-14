---
UID: NF:uxtheme.GetThemeInt
title: GetThemeInt function (uxtheme.h)
description: Retrieves the value of an int property.helpviewer_keywords: ["GetThemeInt","GetThemeInt function [Windows Controls]","controls.GetThemeInt","controls.inet_GetThemeInt","inet_GetThemeInt","inet_GetThemeInt_cpp","uxtheme/GetThemeInt"]
old-location: controls\GetThemeInt.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemeint.htm
ms.date: 12/05/2018
ms.keywords: GetThemeInt, GetThemeInt function [Windows Controls], controls.GetThemeInt, controls.inet_GetThemeInt, inet_GetThemeInt, inet_GetThemeInt_cpp, uxtheme/GetThemeInt
f1_keywords:
- uxtheme/GetThemeInt
dev_langs:
- c++
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
- Ext-MS-Win-UXTheme-Themes-l1-1-0.dll
- xamlpalwp.dll
- ext-ms-win-uxtheme-themes-l1-1-1.dll
api_name:
- GetThemeInt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetThemeInt function


## -description


Retrieves the value of an <b>int</b> property.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://docs.microsoft.com/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the <b>int</b> property. See <a href="https://docs.microsoft.com/windows/desktop/Controls/parts-and-states">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="https://docs.microsoft.com/windows/desktop/Controls/parts-and-states">Parts and States</a>.


### -param iPropId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the property to retrieve. For a list of possible values, see <a href="https://docs.microsoft.com/windows/desktop/Controls/property-typedefs">Property Identifiers</a>.


### -param piVal [out]

Type: <b>int*</b>

Pointer to an <b>int</b> that receives the retrieved value.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/property-typedefs">Property Identifiers</a>
 

 

