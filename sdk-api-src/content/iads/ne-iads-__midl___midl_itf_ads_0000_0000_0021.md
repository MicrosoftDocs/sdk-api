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

# __MIDL___MIDL_itf_ads_0000_0000_0021 enumeration


## -description


The <b>ADS_SCOPEENUM</b> enumeration specifies the scope of a directory search.


## -enum-fields




### -field ADS_SCOPE_BASE

Limits the search to the base object. The result contains, at most, one object.


### -field ADS_SCOPE_ONELEVEL

Searches one level of the immediate children, excluding the base object.


### -field ADS_SCOPE_SUBTREE

Searches the whole subtree, including all the children and the base object itself.


## -remarks



If you do not explicitly set the search scope, the default is <b>ADS_SCOPE_SUBTREE</b>.

Because VBScript cannot read data from a type library, VBScript applications do not recognize the symbolic constants as defined above. Use the numerical constants, instead, to set the appropriate flags in your VBScript applications. To use the symbolic constants as a good programming practice, create explicit declarations of such constants, as done here, in your VBScript applications.


#### Examples

Search scope is one of the search preferences clients can specify. The following code example shows how to accomplish this using the  <a href="https://msdn.microsoft.com/5fc46271-a1be-4a9d-a340-ed801211736a">ADS_SEARCHPREF_INFO</a> structure, together with the elements defined in the  <a href="https://msdn.microsoft.com/f3ab3d53-e53c-459e-929f-f2a3fc95c3ff">ADS_SEARCHPREF_ENUM</a> and this enumeration.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ADS_SEARCHPREF_INFO prefInfo;
prefInfo.dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
prefInfo.vValue.dwType = ADSTYPE_INTEGER;
prefInfo.vValue.Integer = ADS_SCOPE_SUBTREE;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI Enumerations</a>



<a href="https://msdn.microsoft.com/f3ab3d53-e53c-459e-929f-f2a3fc95c3ff">ADS_SEARCHPREF_ENUM</a>



<a href="https://msdn.microsoft.com/5fc46271-a1be-4a9d-a340-ed801211736a">ADS_SEARCHPREF_INFO</a>
 

 

