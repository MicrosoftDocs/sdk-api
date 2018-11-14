---
UID: NE:iads.__MIDL___MIDL_itf_ads_0000_0000_0024
title: "__MIDL___MIDL_itf_ads_0000_0000_0024"
author: windows-sdk-content
description: The ADS_CHASE_REFERRALS_ENUM enumeration specifies if, and how, referral chasing occurs.
old-location: adsi\ads_chase_referrals_enum.htm
tech.root: ADSI
ms.assetid: 1a6ff821-95fe-4993-b503-a8afdedfaeeb
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ADS_CHASE_REFERRALS_ALWAYS, ADS_CHASE_REFERRALS_ENUM, ADS_CHASE_REFERRALS_ENUM enumeration [ADSI], ADS_CHASE_REFERRALS_EXTERNAL, ADS_CHASE_REFERRALS_NEVER, ADS_CHASE_REFERRALS_SUBORDINATE, __MIDL___MIDL_itf_ads_0000_0000_0024, _ds_ads_chase_referrals_enum, adsi.ads__chase__referrals__enum, adsi.ads_chase_referrals_enum, iads/ADS_CHASE_REFERRALS_ALWAYS, iads/ADS_CHASE_REFERRALS_ENUM, iads/ADS_CHASE_REFERRALS_EXTERNAL, iads/ADS_CHASE_REFERRALS_NEVER, iads/ADS_CHASE_REFERRALS_SUBORDINATE
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
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_CHASE_REFERRALS_ENUM
product: Windows
targetos: Windows
req.typenames: ADS_CHASE_REFERRALS_ENUM
req.redist: 
---

# __MIDL___MIDL_itf_ads_0000_0000_0024 enumeration


## -description


The <b>ADS_CHASE_REFERRALS_ENUM</b> enumeration specifies if, and how, referral chasing occurs. When a server determines that other servers hold relevant data, in part or as a whole, it may refer the client to another server to obtain the result. Referral chasing is the action taken by a client to contact the referred-to server to continue the directory search.


## -enum-fields




### -field ADS_CHASE_REFERRALS_NEVER

The client should never chase the referred-to server. Setting this option prevents a client from contacting other servers in a referral process.


### -field ADS_CHASE_REFERRALS_SUBORDINATE

The client chases only subordinate referrals which are a subordinate naming context in a directory tree. For example, if the base search is requested for "DC=Fabrikam,DC=Com", and the server returns a result set and a referral of "DC=Sales,DC=Fabrikam,DC=Com" on the AdbSales server, the client can contact the AdbSales server to continue the search. The ADSI LDAP provider always turns off this flag for paged searches.


### -field ADS_CHASE_REFERRALS_EXTERNAL

The client chases external referrals. For example, a client requests server A to perform a search for "DC=Fabrikam,DC=Com". However, server A does not contain the object, but knows that an independent server, B, owns it. It then refers the client to server B.


### -field ADS_CHASE_REFERRALS_ALWAYS

Referrals are chased for either the subordinate or external type.


## -remarks



Use the constants of this enumeration to set up search preferences for referral chasing. The action amounts to assigning the appropriate fields of the  <a href="https://msdn.microsoft.com/5fc46271-a1be-4a9d-a340-ed801211736a">ADS_SEARCHPREF_INFO</a> structure with elements of the <b>ADS_CHASE_REFERRALS_ENUM</b> and  <a href="https://msdn.microsoft.com/f3ab3d53-e53c-459e-929f-f2a3fc95c3ff">ADS_SEARCHPREF_ENUM</a> enumerations. The values of this enumeration can also be used with  <a href="https://msdn.microsoft.com/1884efe5-86f5-4579-a25e-2ff9c9a6ec2a">IADsObjectOptions</a> to specify whether referral chasing should take place when enumerating the objects under a container object.

The <a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a> interface has a partial implementation of <b>ADS_CHASE_REFERRALS_ENUM</b> through the <a href="https://msdn.microsoft.com/7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc">ChaseReferral</a> property. If the <b>ChaseReferral</b> property is set to zero (0), it is the same as specifying <b>ADS_CHASE_REFERRALS_NEVER</b> (0). If a nonzero value is used, it is the same as specifying <b>ADS_CHASE_REFERRALS_ALWAYS</b> (0x60). <b>IADsNameTranslate</b> does not implement the <b>ADS_CHASE_REFERRALS_SUBORDINATE</b> (0x20) or <b>ADS_CHASE_REFERRALS_EXTERNAL</b> (0x40) options.

The ADSI LDAP provider supports external referrals for paged searches, but does not support subordinate referrals during paging.

<div class="alert"><b>Note</b>  Because VBScript cannot read data from a type library, VBScript applications do not understand the symbolic constants as defined above. You should use the numerical constants instead to set the appropriate flags in your VBScript applications. If you want to use the symbolic constants as a good programming practice, you should make explicit declarations of such constants, as done here, in your VBScript applications.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI
  Enumerations</a>



<a href="https://msdn.microsoft.com/f3ab3d53-e53c-459e-929f-f2a3fc95c3ff">ADS_SEARCHPREF_ENUM</a>



<a href="https://msdn.microsoft.com/5fc46271-a1be-4a9d-a340-ed801211736a">ADS_SEARCHPREF_INFO</a>



<a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a>



<a href="https://msdn.microsoft.com/1884efe5-86f5-4579-a25e-2ff9c9a6ec2a">IADsObjectOptions</a>
 

 

