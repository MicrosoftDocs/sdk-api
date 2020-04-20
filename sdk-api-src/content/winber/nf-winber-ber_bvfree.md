---
UID: NF:winber.ber_bvfree
title: ber_bvfree function (winber.h)
description: The ber_bvfree function frees a berval structure.helpviewer_keywords: ["_ldap_ber_bvfree","ber_bvfree","ber_bvfree function [LDAP]","ldap.ber__bvfree","ldap.ber_bvfree","winber/ber_bvfree","winldap/ber_bvfree"]
old-location: ldap\ber_bvfree.htm
tech.root: ldap
ms.assetid: 9e5a4bb9-568d-48ee-be75-952916c021b1
ms.date: 12/05/2018
ms.keywords: _ldap_ber_bvfree, ber_bvfree, ber_bvfree function [LDAP], ldap.ber__bvfree, ldap.ber_bvfree, winber/ber_bvfree, winldap/ber_bvfree
f1_keywords:
- winber/ber_bvfree
dev_langs:
- c++
req.header: winber.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wldap32.dll
api_name:
- ber_bvfree
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ber_bvfree function


## -description


The <b>ber_bvfree</b> function frees a 
<a href="https://docs.microsoft.com/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structure.


## -parameters




### -param pBerVal [in]

Pointer to the <a href="https://docs.microsoft.com/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structure to be deallocated.


## -returns



None.




## -remarks



Applications should not call this function to free <a href="https://docs.microsoft.com/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structures that they themselves have allocated.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a>
 

 

