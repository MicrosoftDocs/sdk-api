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

# GetThemeAppProperties function


## -description


Retrieves the property flags that control how visual styles are applied in the current application.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The following return values are bit flags combined with a logical OR operator.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STAP_ALLOW_NONCLIENT</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the nonclient areas of application windows have visual styles applied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STAP_ALLOW_CONTROLS</b></dt>
</dl>
</td>
<td width="60%">
Specifies that controls in application windows have visual styles applied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STAP_ALLOW_WEBCONTENT</b></dt>
</dl>
</td>
<td width="60%">
Specifies that all web content displayed in an application is rendered using visual styles.

</td>
</tr>
</table>
 




## -remarks



Individual flags can be extracted from the result by combining the result with the logical AND of the desired flag.

Do not call this function during <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> or global objects constructors. This may cause invalid return values.


#### Examples

The example extracts a single flag's state from the function result.

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




<a href="https://msdn.microsoft.com/7675c2c1-c152-41ad-b34b-5ca6cc7cd26b">SetThemeAppProperties</a>
 

 

