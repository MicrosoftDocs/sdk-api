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

# GetMenuStringA function


## -description


Copies the text string of the specified menu item into the specified buffer. 
<div class="alert"><b>Note</b>  The <b>GetMenuString</b> function has been superseded. Use the <a href="https://msdn.microsoft.com/4a2c9135-510b-4ccf-bdba-35ffabc49d5c">GetMenuItemInfo</a> function to retrieve the menu item text.</div><div> </div>

## -parameters




### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu. 


### -param uIDItem [in]

Type: <b>UINT</b>

The menu item to be changed, as determined by the <i>uFlag</i> parameter. 


### -param lpString [out, optional]

Type: <b>LPTSTR</b>

The buffer that receives the null-terminated string. If the string is as long or longer than <i>lpString</i>, the string is truncated and the terminating null character is added. If <i>lpString</i> is <b>NULL</b>, the function returns the length of the menu string. 


### -param cchMax

TBD


### -param flags

TBD




#### - nMaxCount [in]

Type: <b>int</b>

The maximum length, in characters, of the string to be copied. If the string is longer than the maximum specified in the <i>nMaxCount</i> parameter, the extra characters are truncated. If <i>nMaxCount</i> is 0, the function returns the length of the menu string. 


#### - uFlag [in]

Type: <b>UINT</b>

Indicates how the <i>uIDItem</i> parameter is interpreted. This parameter must be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_BYCOMMAND"></a><a id="mf_bycommand"></a><dl>
<dt><b>MF_BYCOMMAND</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Indicates that <i>uIDItem</i> gives the identifier of the menu item. If neither the <b>MF_BYCOMMAND</b> nor <b>MF_BYPOSITION</b> flag is specified, the <b>MF_BYCOMMAND</b> flag is the default flag.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_BYPOSITION"></a><a id="mf_byposition"></a><dl>
<dt><b>MF_BYPOSITION</b></dt>
<dt>0x00000400L</dt>
</dl>
</td>
<td width="60%">
Indicates that <i>uIDItem</i> gives the zero-based relative position of the menu item.

</td>
</tr>
</table>
 


## -returns



Type: <b>int</b>

If the function succeeds, the return value specifies the number of characters copied to the buffer, not including the terminating null character.

If the function fails, the return value is zero. 

If the specified item is not of type <b>MIIM_STRING</b> or <b>MFT_STRING</b>, then the return value is zero.




## -remarks



The <i>nMaxCount</i> parameter must be one larger than the number of characters in the text string to accommodate the terminating null character. 

If <i>nMaxCount</i> is 0, the function returns the length of the menu string.

<h3><a id="Security_Warning"></a><a id="security_warning"></a><a id="SECURITY_WARNING"></a>Security Warning</h3>
The <i>lpString</i> parameter is a <b>TCHAR</b> buffer, and <i>nMaxCount</i> is the length of the menu string in characters. Sizing these parameters incorrectly can cause truncation of the string, leading to possible loss of data.


#### Examples

For an example, see <a href="using_keyboard_accelerators.htm">Creating User Editable Accelerators</a>. 

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/69ecdcba-177c-4465-95ae-897ed4e96c2d">GetMenuItemID</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>
 

 

