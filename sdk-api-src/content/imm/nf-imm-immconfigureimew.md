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

# ImmConfigureIMEW function


## -description


Displays the configuration dialog box for the IME of the specified input locale identifier.


## -parameters




### -param HKL

TBD


### -param HWND

TBD


### -param DWORD

TBD


### -param LPVOID

TBD




#### - dwMode [in]

Flags specifying the type of dialog box to display. This parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IME_CONFIG_GENERAL"></a><a id="ime_config_general"></a><dl>
<dt><b>IME_CONFIG_GENERAL</b></dt>
</dl>
</td>
<td width="60%">
Display general-purpose configuration dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="IME_CONFIG_REGISTERWORD"></a><a id="ime_config_registerword"></a><dl>
<dt><b>IME_CONFIG_REGISTERWORD</b></dt>
</dl>
</td>
<td width="60%">
Display register word dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="IME_CONFIG_SELECTDICTIONARY"></a><a id="ime_config_selectdictionary"></a><dl>
<dt><b>IME_CONFIG_SELECTDICTIONARY</b></dt>
</dl>
</td>
<td width="60%">
Display dictionary selection dialog box.

</td>
</tr>
</table>
 


#### - hKL [in]

Input locale identifier of an IME.


#### - hWnd [in]

Handle to the parent window for the dialog box.


#### - lpData [in]

Pointer to supplemental data. If <i>dwMode</i> is set to IME_CONFIG_REGISTERWORD, this parameter must indicate a <a href="https://msdn.microsoft.com/70a11a96-a0e3-4741-be91-b85eb38cd767">REGISTERWORD</a> structure. If <i>dwMode</i> is not IME_CONFIG_REGISTERWORD, this parameter is ignored.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>



<a href="https://msdn.microsoft.com/70a11a96-a0e3-4741-be91-b85eb38cd767">REGISTERWORD</a>
 

 

