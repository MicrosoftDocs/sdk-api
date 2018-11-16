---
UID: NF:uxtheme.GetThemePosition
title: GetThemePosition function
author: windows-sdk-content
description: Retrieves the value of a position property.
old-location: controls\GetThemePosition.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemeposition.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetThemePosition, GetThemePosition function [Windows Controls], controls.GetThemePosition, controls.inet_GetThemePosition, inet_GetThemePosition, inet_GetThemePosition_cpp, uxtheme/GetThemePosition
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
 - Ext-MS-Win-UXTheme-Themes-l1-1-0.dll
 - xamlpalwp.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
api_name:
 - GetThemePosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetThemePosition
: 
---

# GetThemePosition function


## -description


Retrieves the value of a position property.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/en-us/library/Bb759821(v=VS.85).aspx">OpenThemeData</a> to create an HTHEME.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the position property. See <a href="https://msdn.microsoft.com/en-us/library/Bb773210(v=VS.85).aspx">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="https://msdn.microsoft.com/en-us/library/Bb773210(v=VS.85).aspx">Parts and States</a>.
	


### -param iPropId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the property to retrieve. For a list of possible values, see <a href="https://msdn.microsoft.com/en-us/library/Bb773213(v=VS.85).aspx">Property Identifiers</a>.


### -param pPoint [out]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that receives the position value.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The part in which the position is located determines the possible state values. For example, if the position is in a check box, the state could be checked or unchecked, but in a caption the possible states are active, inactive, or disabled.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb773213(v=VS.85).aspx">Property Identifiers</a>
 

 

