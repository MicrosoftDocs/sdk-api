---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# GetThemeDocumentationProperty function


## -description


Retrieves the value for a theme property from the documentation section of the specified theme file.


## -parameters




### -param pszThemeName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

Pointer to a string that contains the name of the theme file that will be opened to query for the property.


### -param pszPropertyName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

Pointer to a string that contains the name of the theme property to query. Can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SZ_THDOCPROP_DISPLAYNAME"></a><a id="sz_thdocprop_displayname"></a><dl>
<dt><b>SZ_THDOCPROP_DISPLAYNAME</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the display name of the theme. 

</td>
</tr>
<tr>
<td width="40%"><a id="SZ_THDOCPROP_TOOLTIP"></a><a id="sz_thdocprop_tooltip"></a><dl>
<dt><b>SZ_THDOCPROP_TOOLTIP</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the tooltip associated with this theme.

</td>
</tr>
<tr>
<td width="40%"><a id="SZ_THDOCPROP_AUTHOR"></a><a id="sz_thdocprop_author"></a><dl>
<dt><b>SZ_THDOCPROP_AUTHOR</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the name of the author of the theme.

</td>
</tr>
<tr>
<td width="40%"><a id="SZ_THDOCPROP_CANONICALNAME"></a><a id="sz_thdocprop_canonicalname"></a><dl>
<dt><b>SZ_THDOCPROP_CANONICALNAME</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the name of the theme.

</td>
</tr>
</table>
 


### -param pszValueBuff [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a></b>

Pointer to a string buffer that receives the property string value.


### -param cchMaxValChars [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the maximum number of characters that <i>pszValueBuff</i> can contain.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the theme property has been localized in the theme files string table, this function returns the localized version.



