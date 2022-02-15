---
UID: NE:iads.__MIDL___MIDL_itf_ads_0000_0000_0020
title: ADS_DEREFENUM (iads.h)
description: The ADS_DEREFENUM enumeration specifies the process through which aliases are dereferenced.
helpviewer_keywords: ["ADS_DEREFENUM","ADS_DEREFENUM enumeration [ADSI]","ADS_DEREF_ALWAYS","ADS_DEREF_FINDING","ADS_DEREF_NEVER","ADS_DEREF_SEARCHING","_ds_ads_derefenum","adsi.ads__derefenum","adsi.ads_derefenum","iads/ADS_DEREFENUM","iads/ADS_DEREF_ALWAYS","iads/ADS_DEREF_FINDING","iads/ADS_DEREF_NEVER","iads/ADS_DEREF_SEARCHING"]
old-location: adsi\ads_derefenum.htm
tech.root: adsi
ms.assetid: 4cd080cc-59f9-48e8-93c1-1fccea0238ad
ms.date: 12/05/2018
ms.keywords: ADS_DEREFENUM, ADS_DEREFENUM enumeration [ADSI], ADS_DEREF_ALWAYS, ADS_DEREF_FINDING, ADS_DEREF_NEVER, ADS_DEREF_SEARCHING, _ds_ads_derefenum, adsi.ads__derefenum, adsi.ads_derefenum, iads/ADS_DEREFENUM, iads/ADS_DEREF_ALWAYS, iads/ADS_DEREF_FINDING, iads/ADS_DEREF_NEVER, iads/ADS_DEREF_SEARCHING
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
req.typenames: ADS_DEREFENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0020
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0020
 - ADS_DEREFENUM
 - iads/ADS_DEREFENUM
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
 - ADS_DEREFENUM
---

# ADS_DEREFENUM enumeration


## -description

The <b>ADS_DEREFENUM</b> enumeration specifies the process through which aliases are dereferenced.

## -enum-fields

### -field ADS_DEREF_NEVER:0

Does not dereference aliases when searching or locating the base object of the search.

### -field ADS_DEREF_SEARCHING:1

Dereferences aliases when searching subordinates of the base object, but not when locating the base itself.

### -field ADS_DEREF_FINDING:2

Dereferences aliases when locating the base object of the search, but not when searching its subordinates.

### -field ADS_DEREF_ALWAYS:3

Dereferences aliases when both searching subordinates and locating the base object of the search.

## -remarks

The  <a href="/windows/desktop/api/iads/nn-iads-idirectorysearch">IDirectorySearch</a> interface uses these constants to set the alias dereferencing behavior. If no option is specified, the server defaults to <b>ADS_DEREF_NEVER</b>.

<div class="alert"><b>Note</b>  Because VBScript cannot read data from a type library, VBScript applications do not recognize the symbolic constants as defined above. Use the numerical constants, instead, to set the appropriate flags in your VBScript applications. To use the symbolic constants, as a good programming practice, explicitly declare constants, as done here.</div>
<div> </div>

#### Examples

The following code example shows how to set the search preference for alias dereferencing. m_pSearch refers to a pointer to an object implementing the <a href="/windows/desktop/api/iads/nn-iads-idirectorysearch">IDirectorySearch</a> interface.


```cpp
ADS_SEARCHPREF_INFO prefInfo[1];
HRESULT hr;
 
prefInfo[0].dwSearchPref   = ADS_SEARCHPREF_DEREF_ALIASES;
prefInfo[0].vValue.dwType  = ADSTYPE_INTEGER;
prefInfo[0].vValue.Integer = ADS_DEREF_ALWAYS;
hr = m_pSearch->SetSearchPreference(prefInfo, 1);
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI
  Enumerations</a>



<a href="/windows/desktop/api/iads/nn-iads-idirectorysearch">IDirectorySearch</a>
