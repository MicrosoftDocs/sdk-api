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

# GetThemeSysString function


## -description


Retrieves the value of a system string. 


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to theme data.


### -param iStringId

TBD


### -param pszStringBuff [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a></b>

Pointer to the buffer that receives the string value from this function.


### -param cchMaxStringChars [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the maximum number of characters the string buffer can hold.


#### - iStringID [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies a system string. May be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TMT_CSSNAME"></a><a id="tmt_cssname"></a><dl>
<dt><b>TMT_CSSNAME</b></dt>
</dl>
</td>
<td width="60%">
The name of the CSS file associated with the theme specified by <i>hTheme</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_XMLNAME"></a><a id="tmt_xmlname"></a><dl>
<dt><b>TMT_XMLNAME</b></dt>
</dl>
</td>
<td width="60%">
The name of the XML file associated with the theme specified by <i>hTheme</i>.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the theme data handle is not a <b>NULL</b> handle, this function returns the desired string from the SysMetrics section of the visual style. If the theme data handle is <b>NULL</b>, this function returns the value of the global system metric of the same type.



