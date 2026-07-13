---
UID: NE:iads.__MIDL___MIDL_itf_ads_0000_0000_0021
title: ADS_SCOPEENUM (iads.h)
description: Specifies the scope of a directory search.
helpviewer_keywords: ["ADS_SCOPEENUM","ADS_SCOPEENUM enumeration [ADSI]","ADS_SCOPE_BASE","ADS_SCOPE_ONELEVEL","ADS_SCOPE_SUBTREE","_ds_ads_scopeenum","adsi.ads__scopeenum","adsi.ads_scopeenum","iads/ADS_SCOPEENUM","iads/ADS_SCOPE_BASE","iads/ADS_SCOPE_ONELEVEL","iads/ADS_SCOPE_SUBTREE"]
old-location: adsi\ads_scopeenum.htm
tech.root: adsi
ms.assetid: 403e45fa-bcd6-4422-9111-e9ca9859550a
ms.date: 12/05/2018
ms.keywords: ADS_SCOPEENUM, ADS_SCOPEENUM enumeration [ADSI], ADS_SCOPE_BASE, ADS_SCOPE_ONELEVEL, ADS_SCOPE_SUBTREE, _ds_ads_scopeenum, adsi.ads__scopeenum, adsi.ads_scopeenum, iads/ADS_SCOPEENUM, iads/ADS_SCOPE_BASE, iads/ADS_SCOPE_ONELEVEL, iads/ADS_SCOPE_SUBTREE
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ADS_SCOPEENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0021
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0021
 - ADS_SCOPEENUM
 - iads/ADS_SCOPEENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_SCOPEENUM
---

# ADS_SCOPEENUM enumeration


## -description

The <b>ADS_SCOPEENUM</b> enumeration specifies the scope of a directory search.

## -enum-fields

### -field ADS_SCOPE_BASE:0

Limits the search to the base object. The result contains, at most, one object.

### -field ADS_SCOPE_ONELEVEL:1

Searches one level of the immediate children, excluding the base object.

### -field ADS_SCOPE_SUBTREE:2

Searches the whole subtree, including all the children and the base object itself.

## -remarks

If you do not explicitly set the search scope, the default is <b>ADS_SCOPE_SUBTREE</b>.

Because VBScript cannot read data from a type library, VBScript applications do not recognize the symbolic constants as defined above. Use the numerical constants, instead, to set the appropriate flags in your VBScript applications. To use the symbolic constants as a good programming practice, create explicit declarations of such constants, as done here, in your VBScript applications.


#### Examples

Search scope is one of the search preferences clients can specify. The following code example shows how to accomplish this using the  <a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a> structure, together with the elements defined in the  <a href="/windows/win32/api/iads/ne-iads-ads_searchpref_enum">ADS_SEARCHPREF_ENUM</a> and this enumeration.


```cpp
ADS_SEARCHPREF_INFO prefInfo;
prefInfo.dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
prefInfo.vValue.dwType = ADSTYPE_INTEGER;
prefInfo.vValue.Integer = ADS_SCOPE_SUBTREE;
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI Enumerations</a>



<a href="/windows/win32/api/iads/ne-iads-ads_searchpref_enum">ADS_SEARCHPREF_ENUM</a>



<a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a>
