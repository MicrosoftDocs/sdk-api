---
UID: NF:casetup.IMSCEPSetup.SetAccountInformation
title: IMSCEPSetup::SetAccountInformation (casetup.h)
description: Sets the user account information used by the IIS Network Device Enrollment Service (NDES) extension to perform enrollment on behalf of network devices.
helpviewer_keywords: ["IMSCEPSetup interface [Security]","SetAccountInformation method","IMSCEPSetup.SetAccountInformation","IMSCEPSetup::SetAccountInformation","SetAccountInformation","SetAccountInformation method [Security]","SetAccountInformation method [Security]","IMSCEPSetup interface","casetup/IMSCEPSetup::SetAccountInformation","security.imscepsetup_setaccountinformation"]
old-location: security\imscepsetup_setaccountinformation.htm
tech.root: security
ms.assetid: 32d09bdc-e8e8-4368-9f51-cc7ba170c8a0
ms.date: 12/05/2018
ms.keywords: IMSCEPSetup interface [Security],SetAccountInformation method, IMSCEPSetup.SetAccountInformation, IMSCEPSetup::SetAccountInformation, SetAccountInformation, SetAccountInformation method [Security], SetAccountInformation method [Security],IMSCEPSetup interface, casetup/IMSCEPSetup::SetAccountInformation, security.imscepsetup_setaccountinformation
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSCEPSetup::SetAccountInformation
 - casetup/IMSCEPSetup::SetAccountInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - IMSCEPSetup.SetAccountInformation
---

# IMSCEPSetup::SetAccountInformation


## -description

The <b>SetAccountInformation</b> method sets the user account information used by the IIS Network Device Enrollment Service (NDES) extension to perform enrollment on behalf of network devices.

## -parameters

### -param bstrUserName [in]

A string that contains the name of the user account to use with the IIS extension in the form [<i>DomainName</i>\]<i>UserName</i>.

### -param bstrPassword [in]

A string that contains the password for the user account.

## -remarks

The account must be a member of the <b>IIS_USRS</b> group on the computer.

If NDES is configured for an enterprise <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA), the account must have read permission on the <b>IPSecIntermediateOffline</b> template.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-imscepsetup">IMSCEPSetup</a>