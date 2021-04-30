---
UID: NF:iads.IDirectorySearch.SetSearchPreference
title: IDirectorySearch::SetSearchPreference (iads.h)
description: Specifies a search preference for obtaining data in a subsequent search.
helpviewer_keywords: ["IDirectorySearch interface [ADSI]","SetSearchPreference method","IDirectorySearch.SetSearchPreference","IDirectorySearch::SetSearchPreference","SetSearchPreference","SetSearchPreference method [ADSI]","SetSearchPreference method [ADSI]","IDirectorySearch interface","_ds_idirectorysearch_setsearchpreference","adsi.idirectorysearch__setsearchpreference","adsi.idirectorysearch_setsearchpreference","iads/IDirectorySearch::SetSearchPreference"]
old-location: adsi\idirectorysearch_setsearchpreference.htm
tech.root: adsi
ms.assetid: 1c5b3f72-6165-41ad-99d4-d68bc12ac10b
ms.date: 12/05/2018
ms.keywords: IDirectorySearch interface [ADSI],SetSearchPreference method, IDirectorySearch.SetSearchPreference, IDirectorySearch::SetSearchPreference, SetSearchPreference, SetSearchPreference method [ADSI], SetSearchPreference method [ADSI],IDirectorySearch interface, _ds_idirectorysearch_setsearchpreference, adsi.idirectorysearch__setsearchpreference, adsi.idirectorysearch_setsearchpreference, iads/IDirectorySearch::SetSearchPreference
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
req.dll: Activeds.dll; Adsldp.dll; Adsldpc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectorySearch::SetSearchPreference
 - iads/IDirectorySearch::SetSearchPreference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
 - Adsldp.dll
 - Adsldpc.dll
api_name:
 - IDirectorySearch.SetSearchPreference
---

# IDirectorySearch::SetSearchPreference


## -description

The <b>IDirectorySearch::SetSearchPreference</b> method specifies a search preference for obtaining data in a subsequent search.

## -parameters

### -param pSearchPrefs [in]

Provides a caller-allocated array of  <a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a> structures that contain the search preferences to be set.

### -param dwNumPrefs [in]

Provides the size of the <i>pSearchPrefs</i> array.

## -returns

This method supports the standard return values, as well as the following:

For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a>



<a href="/windows/desktop/api/iads/nn-iads-idirectorysearch">IDirectorySearch</a>