---
UID: NE:iads.__MIDL___MIDL_itf_ads_0000_0000_0019
title: ADS_STATUSENUM (iads.h)
description: Specifies the status of a search preference set with the IDirectorySearch::SetSearchPreference method.
helpviewer_keywords: ["*PADS_STATUS","ADS_STATUS","ADS_STATUSENUM","ADS_STATUSENUM enumeration [ADSI]","ADS_STATUS_INVALID_SEARCHPREF","ADS_STATUS_INVALID_SEARCHPREFVALUE","ADS_STATUS_S_OK","_ds_ads_statusenum","adsi.ads__statusenum","adsi.ads_statusenum","iads/ADS_STATUSENUM","iads/ADS_STATUS_INVALID_SEARCHPREF","iads/ADS_STATUS_INVALID_SEARCHPREFVALUE","iads/ADS_STATUS_S_OK"]
old-location: adsi\ads_statusenum.htm
tech.root: adsi
ms.assetid: dfc080da-f849-4df3-9b14-1193b9303742
ms.date: 12/05/2018
ms.keywords: '*PADS_STATUS, ADS_STATUS, ADS_STATUSENUM, ADS_STATUSENUM enumeration [ADSI], ADS_STATUS_INVALID_SEARCHPREF, ADS_STATUS_INVALID_SEARCHPREFVALUE, ADS_STATUS_S_OK, _ds_ads_statusenum, adsi.ads__statusenum, adsi.ads_statusenum, iads/ADS_STATUSENUM, iads/ADS_STATUS_INVALID_SEARCHPREF, iads/ADS_STATUS_INVALID_SEARCHPREFVALUE, iads/ADS_STATUS_S_OK'
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
req.typenames: ADS_STATUSENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0019
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0019
 - ADS_STATUSENUM
 - iads/ADS_STATUSENUM
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
 - ADS_STATUSENUM
---

# ADS_STATUSENUM enumeration


## -description

The <b>ADS_STATUSENUM</b> enumeration specifies the status of a search preference set with the <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference">IDirectorySearch::SetSearchPreference</a> method.

## -enum-fields

### -field ADS_STATUS_S_OK:0

The search preference was set successfully.

### -field ADS_STATUS_INVALID_SEARCHPREF

The search preference specified in the <b>dwSearchPref</b> member of the  <a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a> structure is invalid. Search preferences must be taken from the  <a href="/windows/win32/api/iads/ne-iads-ads_searchpref_enum">ADS_SEARCHPREF_ENUM</a> enumeration.

### -field ADS_STATUS_INVALID_SEARCHPREFVALUE

The value specified in the <b>vValue</b> member of the <a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a> structure is invalid for the corresponding search preference.

## -remarks

The  <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference">IDirectorySearch::SetSearchPreference</a> method sets the <b>dwStatus</b> member <a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a> structure to one of the <b>ADS_STATUSENUM</b> values to indicate the status of the corresponding search preference. Callers can use this status value to decide whether to execute a search.

The <b>ADS_STATUS_INVALID_SEARCHPREF</b> status value may be set if you set a valid search preference, but that preference is not supported. For example, if you set <b>ADS_SEARCHPREF_SORT_ON</b>, but the server you communicate with does not support the LDAP server-side sort control, the <b>dwStatus</b> member of the  <a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a> structure is set to <b>ADS_STATUS_INVALID_SEARCHPREF</b> by the <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference">IDirectorySearch::SetSearchPreference</a> call.

<div class="alert"><b>Note</b>  Because VBScript cannot read data from a type library, VBScript applications do not recognize the symbolic constants as defined above. You should use the numeric constants instead to set the appropriate flags in your VBScript applications. To use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done in the following code example.</div>
<div> </div>

#### Examples

The following code example shows how to use the <b>ADS_STATUSENUM</b> enumeration with the <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference">IDirectorySearch::SetSearchPreference</a> method to determine the status of a search preference.


```cpp
/***************************************************************************

    SetAndCheckSearchTimeout()

***************************************************************************/

HRESULT SetAndCheckSearchTimeout(IDirectorySearch *pSearch, 
                                 DWORD dwTimeout, 
                                 ADS_STATUSENUM *pStatus)
{
    if(!pSearch || !pStatus)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr;
    ADS_SEARCHPREF_INFO SearchPref;

    SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
    SearchPref.vValue.dwType = ADSTYPE_INTEGER;
    SearchPref.vValue.Integer = dwTimeout;
    SearchPref.dwStatus = ADS_STATUS_S_OK;

    hr = pSearch->SetSearchPreference(&SearchPref, 1);
    if(S_OK != hr)
    {
        return hr;
    }

    *pStatus = SearchPref.dwStatus;
    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI
    Enumerations</a>



<a href="/windows/win32/api/iads/ne-iads-ads_searchpref_enum">ADS_SEARCHPREF_ENUM</a>



<a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference">IDirectorySearch::SetSearchPreference</a>
