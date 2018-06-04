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

# __MIDL___MIDL_itf_ads_0000_0000_0020 enumeration


## -description


The <b>ADS_DEREFENUM</b> enumeration specifies the process through which aliases are dereferenced.


## -enum-fields




### -field ADS_DEREF_NEVER

Does not dereference aliases when searching or locating the base object of the search.


### -field ADS_DEREF_SEARCHING

Dereferences aliases when searching subordinates of the base object, but not when locating the base itself.


### -field ADS_DEREF_FINDING

Dereferences aliases when locating the base object of the search, but not when searching its subordinates.


### -field ADS_DEREF_ALWAYS

Dereferences aliases when both searching subordinates and locating the base object of the search.


## -remarks



The  <a href="https://msdn.microsoft.com/e8989795-8f72-476a-a69e-c0e8800289ab">IDirectorySearch</a> interface uses these constants to set the alias dereferencing behavior. If no option is specified, the server defaults to <b>ADS_DEREF_NEVER</b>.

<div class="alert"><b>Note</b>  Because VBScript cannot read data from a type library, VBScript applications do not recognize the symbolic constants as defined above. Use the numerical constants, instead, to set the appropriate flags in your VBScript applications. To use the symbolic constants, as a good programming practice, explicitly declare constants, as done here.</div>
<div> </div>

#### Examples

The following code example shows how to set the search preference for alias dereferencing. m_pSearch refers to a pointer to an object implementing the <a href="https://msdn.microsoft.com/e8989795-8f72-476a-a69e-c0e8800289ab">IDirectorySearch</a> interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ADS_SEARCHPREF_INFO prefInfo[1];
HRESULT hr;
 
prefInfo[0].dwSearchPref   = ADS_SEARCHPREF_DEREF_ALIASES;
prefInfo[0].vValue.dwType  = ADSTYPE_INTEGER;
prefInfo[0].vValue.Integer = ADS_DEREF_ALWAYS;
hr = m_pSearch-&gt;SetSearchPreference(prefInfo, 1);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI
  Enumerations</a>



<a href="https://msdn.microsoft.com/e8989795-8f72-476a-a69e-c0e8800289ab">IDirectorySearch</a>
 

 

