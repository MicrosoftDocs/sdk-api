---
UID: NF:winldap.LdapMapErrorToWin32
title: LdapMapErrorToWin32 function (winldap.h)
description: The LdapMapErrorToWin32 function translates an LdapError value to the closest Win32 error code.
helpviewer_keywords: ["LdapMapErrorToWin32","LdapMapErrorToWin32 function [LDAP]","_ldap_ldapmaperrortowin32","ldap.ldapmaperrortowin32","winldap/LdapMapErrorToWin32"]
old-location: ldap\ldapmaperrortowin32.htm
tech.root: ldap
ms.assetid: 5fdbac24-a1fb-41b2-924c-918bf7e0028a
ms.date: 12/05/2018
ms.keywords: LdapMapErrorToWin32, LdapMapErrorToWin32 function [LDAP], _ldap_ldapmaperrortowin32, ldap.ldapmaperrortowin32, winldap/LdapMapErrorToWin32
req.header: winldap.h
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
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LdapMapErrorToWin32
 - winldap/LdapMapErrorToWin32
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - LdapMapErrorToWin32
---

# LdapMapErrorToWin32 function


## -description

The <b>LdapMapErrorToWin32</b> function translates an LdapError value to the closest Win32 error code.

## -parameters

### -param LdapError [in]

The error code returned from an LDAP function.

## -returns

Returns the corresponding Win32 error code.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a>