---
UID: NF:gpedit.IGPEInformation.GetHint
title: IGPEInformation::GetHint (gpedit.h)
description: The GetHint method retrieves the type of Active Directory object to which this GPO can be linked.
helpviewer_keywords: ["GPHintDomain","GPHintMachine","GPHintOrganizationalUnit","GPHintSite","GPHintUnknown","GetHint","GetHint method [Group Policy]","GetHint method [Group Policy]","IGPEInformation interface","IGPEInformation interface [Group Policy]","GetHint method","IGPEInformation.GetHint","IGPEInformation::GetHint","_win32_igpeinformation_gethint","gpedit/IGPEInformation::GetHint","policy.igpeinformation_gethint"]
old-location: policy\igpeinformation_gethint.htm
tech.root: Policy
ms.assetid: 4e63c6b7-ae4f-4789-bfcc-8a066fb6ad02
ms.date: 12/05/2018
ms.keywords: GPHintDomain, GPHintMachine, GPHintOrganizationalUnit, GPHintSite, GPHintUnknown, GetHint, GetHint method [Group Policy], GetHint method [Group Policy],IGPEInformation interface, IGPEInformation interface [Group Policy],GetHint method, IGPEInformation.GetHint, IGPEInformation::GetHint, _win32_igpeinformation_gethint, gpedit/IGPEInformation::GetHint, policy.igpeinformation_gethint
req.header: gpedit.h
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
req.dll: Gpedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPEInformation::GetHint
 - gpedit/IGPEInformation::GetHint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGPEInformation.GetHint
---

# IGPEInformation::GetHint


## -description

The
    <b>GetHint</b> method retrieves the type of Active Directory object to which this GPO can be linked.

## -parameters

### -param gpHint [out]

Receives the directory service type. This parameter can be one of the following values.



#### GPHintUnknown

No link information is available.



#### GPHintMachine

The object can be linked to a computer (local or remote).



#### GPHintSite

The object can be linked to a site.



#### GPHintDomain

The object can be linked to a domain.



#### GPHintOrganizationalUnit

The object can be linked to an organizational unit.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

The Group Policy Object Editor cannot determine which Active Directory objects are linked to a particular GPO. The 
<b>GetHint</b> method provides linking information based on how the user started the Group Policy Object Editor. It can be started in the following ways:

<ul>
<li>As an extension to the Active Directory Manager. Navigate to the site, domain, or organizational unit, then select <a href="/previous-versions/windows/desktop/Policy/group-policy-start-page">Group Policy</a>.</li>
<li>As a stand-alone MMC tool with a specific link.</li>
<li>As a stand-alone MMC tool without a specific link.</li>
</ul>
You may want to customize your application's user interface based on the result of calling this method. However, use this method with caution because the returned value may indicate the wrong scope.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igpeinformation">IGPEInformation</a>