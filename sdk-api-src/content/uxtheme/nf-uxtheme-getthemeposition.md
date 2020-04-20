---
UID: NF:uxtheme.GetThemePosition
title: GetThemePosition function (uxtheme.h)
description: Retrieves the value of a position property.helpviewer_keywords: ["GetThemePosition","GetThemePosition function [Windows Controls]","controls.GetThemePosition","controls.inet_GetThemePosition","inet_GetThemePosition","inet_GetThemePosition_cpp","uxtheme/GetThemePosition"]
old-location: controls\GetThemePosition.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemeposition.htm
ms.date: 12/05/2018
ms.keywords: GetThemePosition, GetThemePosition function [Windows Controls], controls.GetThemePosition, controls.inet_GetThemePosition, inet_GetThemePosition, inet_GetThemePosition_cpp, uxtheme/GetThemePosition
f1_keywords:
- uxtheme/GetThemePosition
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
- GetThemePosition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetThemePosition function


## -description


Retrieves the value of a position property.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://docs.microsoft.com/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the position property. See <a href="https://docs.microsoft.com/windows/desktop/Controls/parts-and-states">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="https://docs.microsoft.com/windows/desktop/Controls/parts-and-states">Parts and States</a>.
	


### -param iPropId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the property to retrieve. For a list of possible values, see <a href="https://docs.microsoft.com/windows/desktop/Controls/property-typedefs">Property Identifiers</a>.


### -param pPoint [out]

Type: <b><a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a> structure that receives the position value.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The part in which the position is located determines the possible state values. For example, if the position is in a check box, the state could be checked or unchecked, but in a caption the possible states are active, inactive, or disabled.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/property-typedefs">Property Identifiers</a>
 

 

