---
UID: NE:iads.__MIDL___MIDL_itf_ads_0000_0000_0024
title: ADS_CHASE_REFERRALS_ENUM (iads.h)
description: The ADS_CHASE_REFERRALS_ENUM enumeration specifies if, and how, referral chasing occurs.
helpviewer_keywords: ["ADS_CHASE_REFERRALS_ALWAYS","ADS_CHASE_REFERRALS_ENUM","ADS_CHASE_REFERRALS_ENUM enumeration [ADSI]","ADS_CHASE_REFERRALS_EXTERNAL","ADS_CHASE_REFERRALS_NEVER","ADS_CHASE_REFERRALS_SUBORDINATE","_ds_ads_chase_referrals_enum","adsi.ads__chase__referrals__enum","adsi.ads_chase_referrals_enum","iads/ADS_CHASE_REFERRALS_ALWAYS","iads/ADS_CHASE_REFERRALS_ENUM","iads/ADS_CHASE_REFERRALS_EXTERNAL","iads/ADS_CHASE_REFERRALS_NEVER","iads/ADS_CHASE_REFERRALS_SUBORDINATE"]
old-location: adsi\ads_chase_referrals_enum.htm
tech.root: adsi
ms.assetid: 1a6ff821-95fe-4993-b503-a8afdedfaeeb
ms.date: 12/05/2018
ms.keywords: ADS_CHASE_REFERRALS_ALWAYS, ADS_CHASE_REFERRALS_ENUM, ADS_CHASE_REFERRALS_ENUM enumeration [ADSI], ADS_CHASE_REFERRALS_EXTERNAL, ADS_CHASE_REFERRALS_NEVER, ADS_CHASE_REFERRALS_SUBORDINATE, _ds_ads_chase_referrals_enum, adsi.ads__chase__referrals__enum, adsi.ads_chase_referrals_enum, iads/ADS_CHASE_REFERRALS_ALWAYS, iads/ADS_CHASE_REFERRALS_ENUM, iads/ADS_CHASE_REFERRALS_EXTERNAL, iads/ADS_CHASE_REFERRALS_NEVER, iads/ADS_CHASE_REFERRALS_SUBORDINATE
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
req.typenames: ADS_CHASE_REFERRALS_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0024
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0024
 - ADS_CHASE_REFERRALS_ENUM
 - iads/ADS_CHASE_REFERRALS_ENUM
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
 - ADS_CHASE_REFERRALS_ENUM
---

# ADS_CHASE_REFERRALS_ENUM enumeration


## -description

The <b>ADS_CHASE_REFERRALS_ENUM</b> enumeration specifies if, and how, referral chasing occurs. When a server determines that other servers hold relevant data, in part or as a whole, it may refer the client to another server to obtain the result. Referral chasing is the action taken by a client to contact the referred-to server to continue the directory search.

## -enum-fields

### -field ADS_CHASE_REFERRALS_NEVER:0

The client should never chase the referred-to server. Setting this option prevents a client from contacting other servers in a referral process.

### -field ADS_CHASE_REFERRALS_SUBORDINATE:0x20

The client chases only subordinate referrals which are a subordinate naming context in a directory tree. For example, if the base search is requested for "DC=Fabrikam,DC=Com", and the server returns a result set and a referral of "DC=Sales,DC=Fabrikam,DC=Com" on the AdbSales server, the client can contact the AdbSales server to continue the search. The ADSI LDAP provider always turns off this flag for paged searches.

### -field ADS_CHASE_REFERRALS_EXTERNAL:0x40

The client chases external referrals. For example, a client requests server A to perform a search for "DC=Fabrikam,DC=Com". However, server A does not contain the object, but knows that an independent server, B, owns it. It then refers the client to server B.

### -field ADS_CHASE_REFERRALS_ALWAYS

Referrals are chased for either the subordinate or external type.

## -remarks

Use the constants of this enumeration to set up search preferences for referral chasing. The action amounts to assigning the appropriate fields of the  <a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a> structure with elements of the <b>ADS_CHASE_REFERRALS_ENUM</b> and  <a href="/windows/win32/api/iads/ne-iads-ads_searchpref_enum">ADS_SEARCHPREF_ENUM</a> enumerations. The values of this enumeration can also be used with  <a href="/windows/desktop/api/iads/nn-iads-iadsobjectoptions">IADsObjectOptions</a> to specify whether referral chasing should take place when enumerating the objects under a container object.

The <a href="/windows/desktop/api/iads/nn-iads-iadsnametranslate">IADsNameTranslate</a> interface has a partial implementation of <b>ADS_CHASE_REFERRALS_ENUM</b> through the <a href="/windows/desktop/ADSI/iadsnametranslate-property-methods">ChaseReferral</a> property. If the <b>ChaseReferral</b> property is set to zero (0), it is the same as specifying <b>ADS_CHASE_REFERRALS_NEVER</b> (0). If a nonzero value is used, it is the same as specifying <b>ADS_CHASE_REFERRALS_ALWAYS</b> (0x60). <b>IADsNameTranslate</b> does not implement the <b>ADS_CHASE_REFERRALS_SUBORDINATE</b> (0x20) or <b>ADS_CHASE_REFERRALS_EXTERNAL</b> (0x40) options.

The ADSI LDAP provider supports external referrals for paged searches, but does not support subordinate referrals during paging.

<div class="alert"><b>Note</b>  Because VBScript cannot read data from a type library, VBScript applications do not understand the symbolic constants as defined above. You should use the numerical constants instead to set the appropriate flags in your VBScript applications. If you want to use the symbolic constants as a good programming practice, you should make explicit declarations of such constants, as done here, in your VBScript applications.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI
  Enumerations</a>



<a href="/windows/win32/api/iads/ne-iads-ads_searchpref_enum">ADS_SEARCHPREF_ENUM</a>



<a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsnametranslate">IADsNameTranslate</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsobjectoptions">IADsObjectOptions</a>
