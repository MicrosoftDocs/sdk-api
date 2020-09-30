---
UID: NF:winldap.ldap_cleanup
title: ldap_cleanup function (winldap.h)
description: Warning  The ldap_cleanup function may cause unpredictable behavior at DLL unload time so, there is no way to safely clean up resources when dynamically loading and unloading the wldap32.dll.Because of this, resource leaks can occur on unload of the library. Use of ldap_cleanup is therefore not recommended and, is at your own risk. .
helpviewer_keywords: ["ldap.ldap_cleanup","ldap_cleanup","ldap_cleanup function [LDAP]","winldap/ldap_cleanup"]
old-location: ldap\ldap_cleanup.htm
tech.root: ldap
ms.assetid: AAB2A6D4-7AF1-4E9D-9D76-28B991F732CE
ms.date: 12/05/2018
ms.keywords: ldap.ldap_cleanup, ldap_cleanup, ldap_cleanup function [LDAP], winldap/ldap_cleanup
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
 - ldap_cleanup
 - winldap/ldap_cleanup
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
 - ldap_cleanup
---

# ldap_cleanup function


## -description

<div class="alert"><b>Warning</b>  <p class="note">The <b>ldap_cleanup</b> function may cause unpredictable 
      behavior at DLL unload time so, there is no way to safely clean up resources when dynamically loading and 
      unloading the wldap32.dll.

<p class="note">Because of this, resource leaks can occur on unload of the library. Use of 
      <b>ldap_cleanup</b> is therefore not recommended and, is at 
      your own risk.

</div>
<div> </div>

## -parameters

### -param hInstance

This parameter is ignored.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
       <a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

<div class="alert"><b>Warning</b>  The <b>ldap_cleanup</b> function may cause 
    unpredictable behavior at the DLL unload time.  Use is not recommended and is at your own risk.</div>
<div> </div>