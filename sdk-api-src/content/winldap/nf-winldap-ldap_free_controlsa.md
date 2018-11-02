---
UID: NF:winldap.ldap_free_controlsA
title: ldap_free_controlsA function
author: windows-sdk-content
description: Obsolete function which frees an array of LDAPControl structures.
old-location: ldap\ldap_free_controls.htm
tech.root: ldap
ms.assetid: 0c663189-5aa7-4dad-b265-c9af873bf576
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "_ldap_ldap_free_controls, ldap.ldap__free__controls, ldap.ldap_free_controls, ldap_free_controls, ldap_free_controls function [LDAP], ldap_free_controlsA, ldap_free_controlsW, winldap/ldap_free_controls, winldap/ldap_free_controlsA, winldap/ldap_free_controlsW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_free_controlsW (Unicode) and ldap_free_controlsA (ANSI)
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
 - ldap_free_controls
 - ldap_free_controlsA
 - ldap_free_controlsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_free_controlsA function


## -description


This function is not supported.

The <b>ldap_free_controls</b> function is an 
   obsolete function which frees an array of 
   <a href="https://msdn.microsoft.com/c0b4d712-021d-46f3-8bda-aaf660ec1acc">LDAPControl</a> structures.
<div class="alert"><b>Note</b>  Obsolete. Use the <a href="https://msdn.microsoft.com/e1e4545f-6184-41bb-bba1-4eebae9cdaaf">ldap_controls_free</a> 
    function.</div><div> </div>

## -parameters




### -param Controls [in]

The array of <a href="https://msdn.microsoft.com/c0b4d712-021d-46f3-8bda-aaf660ec1acc">LDAPControl</a> structures to free.


## -returns



If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see 
       <a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.



