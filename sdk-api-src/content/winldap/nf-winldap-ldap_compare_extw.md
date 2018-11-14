---
UID: NF:winldap.ldap_compare_extW
title: ldap_compare_extW function
author: windows-sdk-content
description: Use the ldap_compare_ext function to determine if an attribute, for a given entry, holds a known value.
old-location: ldap\ldap_compare_ext.htm
tech.root: ldap
ms.assetid: 07e96a95-439b-4bb1-a9ca-d76d181e8bea
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "_ldap_ldap_compare_ext, ldap.ldap__compare__ext, ldap.ldap_compare_ext, ldap_compare_ext, ldap_compare_ext function [LDAP], ldap_compare_extA, ldap_compare_extW, winldap/ldap_compare_ext, winldap/ldap_compare_extA, winldap/ldap_compare_extW"
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
req.unicode-ansi: ldap_compare_extW (Unicode) and ldap_compare_extA (ANSI)
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
 - ldap_compare_ext
 - ldap_compare_extA
 - ldap_compare_extW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ldap_compare_extW
: 
---

# ldap_compare_extW function


## -description


Use the <b>ldap_compare_ext</b> function to determine if an attribute, for a given entry, holds a known value.


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to compare.


### -param Attr [in]

A pointer to a null-terminated string that contains the attribute to compare.


### -param Value [in]

A pointer to a null-terminated string that contains the string attribute value to be compared to the attribute value.


### -param Data [in]

The 
<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> attribute value to be compared to the attribute value.


### -param ServerControls [in]

Optional. A list of LDAP server controls. This parameter should be set to <b>NULL</b> if not used.


### -param ClientControls [in]

Optional. A list of client controls. This parameter should be set to <b>NULL</b> if not used.


### -param MessageNumber [out]

The message ID for the compare operation.


## -returns



If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a> for more information.




## -remarks



The <b>ldap_compare_ext</b> function initiates an asynchronous compare operation, comparing the value of an attribute to a known value. The parameters and effects of <b>ldap_compare_ext</b> subsume those of 
<a href="https://msdn.microsoft.com/0cdcea2f-5ee2-407a-a229-5a3fb1e3b856">ldap_compare</a>. The extended routine includes additional parameters to support client and server controls, comparison of binary values, and thread safety.

Use the <i>Value</i> parameter for comparing string values or use the <i>Data</i> parameter for comparing raw binary data. Set the unused parameter to <b>NULL</b>. If neither parameter is <b>NULL</b>, the compare operation will use the value in the <i>Data</i> parameter.

If successful, <b>ldap_compare_ext</b> passes back the message ID for the operation in the <i>MessageNumber</i> parameter. Call 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> with the message ID to obtain the result of the compare. To have the function return the compare result directly, use the synchronous extended compare function 
<a href="https://msdn.microsoft.com/b22568b1-5043-422e-9c4e-cc51cc77d143">ldap_compare_ext_s</a>.

Multithreading: Calls to <b>ldap_compare_ext</b> are thread-safe.




## -see-also




<a href="https://msdn.microsoft.com/3e1e29ff-43ec-4cc3-9414-41b7c61f8b42">Extended Controls</a>



<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/2c1f68e6-51b0-4270-b55a-88ba7292bbbc">Using Controls</a>



<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a>



<a href="https://msdn.microsoft.com/0cdcea2f-5ee2-407a-a229-5a3fb1e3b856">ldap_compare</a>



<a href="https://msdn.microsoft.com/b22568b1-5043-422e-9c4e-cc51cc77d143">ldap_compare_ext_s</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>
 

 

