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

# GetThemeSysFont function


## -description


Retrieves the <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> of a system font.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to theme data.


### -param iFontId

TBD


### -param plf [out]

Type: <b>LOGFONTW*</b>

Pointer to a <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure that receives the font information from this function.



#### - iFontID [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies a system font. May be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TMT_CAPTIONFONT"></a><a id="tmt_captionfont"></a><dl>
<dt><b>TMT_CAPTIONFONT</b></dt>
</dl>
</td>
<td width="60%">
The font used by window captions.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_SMALLCAPTIONFONT"></a><a id="tmt_smallcaptionfont"></a><dl>
<dt><b>TMT_SMALLCAPTIONFONT</b></dt>
</dl>
</td>
<td width="60%">
The font used by window small captions.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_MENUFONT"></a><a id="tmt_menufont"></a><dl>
<dt><b>TMT_MENUFONT</b></dt>
</dl>
</td>
<td width="60%">
The font used by menus.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_STATUSFONT"></a><a id="tmt_statusfont"></a><dl>
<dt><b>TMT_STATUSFONT</b></dt>
</dl>
</td>
<td width="60%">
The font used in status messages.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_MSGBOXFONT"></a><a id="tmt_msgboxfont"></a><dl>
<dt><b>TMT_MSGBOXFONT</b></dt>
</dl>
</td>
<td width="60%">
The font used to display messages in a message box.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_ICONTITLEFONT"></a><a id="tmt_icontitlefont"></a><dl>
<dt><b>TMT_ICONTITLEFONT</b></dt>
</dl>
</td>
<td width="60%">
The font used for icons.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function requires vssym32.h and uxtheme.h.

If the theme data handle is not a <b>NULL</b> handle, this function returns the desired <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> from the SysMetrics section of the visual style. If the theme data handle is <b>NULL</b>, the function returns the value of the global system metric of the same type.

The font is scaled in dots per inch for the current logical screen.



