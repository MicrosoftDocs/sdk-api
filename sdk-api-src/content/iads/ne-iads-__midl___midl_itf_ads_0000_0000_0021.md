---
UID: NE:iads.__MIDL___MIDL_itf_ads_0000_0000_0021
title: "__MIDL___MIDL_itf_ads_0000_0000_0021"
author: windows-driver-content
description: Specifies the scope of a directory search.
old-location: adsi\ads_scopeenum.htm
old-project: ADSI
ms.assetid: 403e45fa-bcd6-4422-9111-e9ca9859550a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ADS_SCOPEENUM, ADS_SCOPEENUM enumeration [ADSI], ADS_SCOPE_BASE, ADS_SCOPE_ONELEVEL, ADS_SCOPE_SUBTREE, __MIDL___MIDL_itf_ads_0000_0000_0021, _ds_ads_scopeenum, adsi.ads__scopeenum, adsi.ads_scopeenum, iads/ADS_SCOPEENUM, iads/ADS_SCOPE_BASE, iads/ADS_SCOPE_ONELEVEL, iads/ADS_SCOPE_SUBTREE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: IAccess.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ADS_SCOPEENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iads.h
api_name:
-	ADS_SCOPEENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

