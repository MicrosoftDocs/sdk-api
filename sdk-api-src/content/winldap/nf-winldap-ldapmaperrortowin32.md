---
UID: NF:winldap.LdapMapErrorToWin32
title: LdapMapErrorToWin32 function
author: windows-sdk-content
description: The LdapMapErrorToWin32 function translates an LdapError value to the closest Win32 error code.
old-location: ldap\ldapmaperrortowin32.htm
old-project: LDAP
ms.assetid: 5fdbac24-a1fb-41b2-924c-918bf7e0028a
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: LdapMapErrorToWin32, LdapMapErrorToWin32 function [LDAP], _ldap_ldapmaperrortowin32, ldap.ldapmaperrortowin32, winldap/LdapMapErrorToWin32
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, *PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wldap32.dll
api_name:
-	LdapMapErrorToWin32
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
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




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/04bcdd90-344a-4f2d-a700-e725584e49d9">LdapGetLastError</a>
 

 

