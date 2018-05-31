---
UID: NF:uxtheme.GetThemeBackgroundContentRect
title: GetThemeBackgroundContentRect function
author: windows-sdk-content
description: Retrieves the size of the content area for the background defined by the visual style.
old-location: controls\GetThemeBackgroundContentRect.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemebackgroundcontentrect.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetThemeBackgroundContentRect, GetThemeBackgroundContentRect function [Windows Controls], controls.GetThemeBackgroundContentRect, controls.inet_GetThemeBackgroundContentRect, inet_GetThemeBackgroundContentRect, inet_GetThemeBackgroundContentRect_cpp, uxtheme/GetThemeBackgroundContentRect
ms.prod: windows
ms.technology: windows-sdk
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
-	ext-ms-win-uxtheme-themes-l1-1-1.dll
-	xamlpalwp.dll
api_name:
-	GetThemeBackgroundContentRect
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# GetThemeBackgroundContentRect function


## -description


Retrieves the size of the content area for the background defined by the visual style.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/3c496a3f-e4d0-4938-af66-85df93829cd8">OpenThemeData</a> to create an HTHEME.


### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

HDC to use when drawing. This parameter may be set to <b>NULL</b>.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the content area. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part that contains the content area. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param pBoundingRect [in]

Type: <b>LPCRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the total background rectangle, in logical coordinates. This is the area inside the borders or margins.


### -param pContentRect [out]

Type: <b>LPRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that receives the content area background rectangle, in logical coordinates.  This rectangle is calculated to fit the content area.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A visual style can define a content area within each background image. This is the area where content such as text and icons can be placed without overwriting background borders.


#### Examples


		When applying a theme to an entire client area of a window, you can call <a href="https://msdn.microsoft.com/3746920a-8333-411c-a0f2-4e44b9cce973">GetClientRect</a> to retrieve this area in a <b>RECT</b>, which can be passed via pointer as the <i>pContentRect</i> parameter to <b>GetThemeBackgroundContentRect</b> as in the following example.
		

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DWORD resultFlags = GetThemeAppProperties();
bool ctrlsAreThemed = ((resultFlags &amp; STAP_ALLOW_CONTROLS) != 0);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3db9c648-f040-475f-bb5f-59f138b6ed2e">GetThemeBackgroundExtent</a>



<a href="https://msdn.microsoft.com/b0e22022-fea9-43d1-8ef0-7a1c518760f1">Property Identifiers</a>



<b>Reference</b>
 

 

