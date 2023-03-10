---
UID: NF:uxtheme.GetThemeSysString
title: GetThemeSysString function (uxtheme.h)
description: Retrieves the value of a system string.
helpviewer_keywords: ["GetThemeSysString","GetThemeSysString function [Windows Controls]","TMT_CSSNAME","TMT_XMLNAME","controls.GetThemeSysString","controls.inet_GetThemeSysString","inet_GetThemeSysString","inet_GetThemeSysString_cpp","uxtheme/GetThemeSysString"]
old-location: controls\GetThemeSysString.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemesysstring.htm
ms.date: 12/05/2018
ms.keywords: GetThemeSysString, GetThemeSysString function [Windows Controls], TMT_CSSNAME, TMT_XMLNAME, controls.GetThemeSysString, controls.inet_GetThemeSysString, inet_GetThemeSysString, inet_GetThemeSysString_cpp, uxtheme/GetThemeSysString
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetThemeSysString
 - uxtheme/GetThemeSysString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - GetThemeSysString
---

# GetThemeSysString function


## -description

Retrieves the value of a system string.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to theme data.

### -param iStringId [in]

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

### -param pszStringBuff [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a></b>

Pointer to the buffer that receives the string value from this function.

### -param cchMaxStringChars [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the maximum number of characters the string buffer can hold.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the theme data handle is not a <b>NULL</b> handle, this function returns the desired string from the SysMetrics section of the visual style. If the theme data handle is <b>NULL</b>, this function returns the value of the global system metric of the same type.