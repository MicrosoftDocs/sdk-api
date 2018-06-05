---
UID: NF:winldap.ldap_extended_operation_sW
title: ldap_extended_operation_sW function
author: windows-sdk-content
description: Used to pass extended LDAP operations to the server.
old-location: ldap\ldap_extended_operation_s.htm
old-project: LDAP
ms.assetid: a9e354f3-b6b3-4c41-93d7-497354c87237
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: ldap.ldap_extended_operation_s, ldap_extended_operation_s, ldap_extended_operation_s function [LDAP], ldap_extended_operation_sA, ldap_extended_operation_sW, winldap/ldap_extended_operation_s, winldap/ldap_extended_operation_sA, winldap/ldap_extended_operation_sW
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
req.unicode-ansi: ldap_extended_operation_sW (Unicode) and ldap_extended_operation_sA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, *PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wldap32.dll
api_name:
-	ldap_extended_operation_s
-	ldap_extended_operation_sA
-	ldap_extended_operation_sW
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_extended_operation_sW function


## -description


The <b>ldap_extended_operation_s</b> function is used to pass extended LDAP operations to the server.


## -parameters




### -param ExternalHandle

TBD


### -param Oid [in]

A pointer to a null-terminated string that contains the dotted object identifier (OID) text string that names the request.


### -param Data [in]

The arbitrary data required by the operation. If <b>NULL</b>, no data is sent to the server.


### -param ServerControls [in]

Optional. A list of LDAP server controls. Set this parameter to <b>NULL</b> if not used.


### -param ClientControls [in]

Optional. A list of client controls. Set this parameter to <b>NULL</b> if not used.


### -param ReturnedOid [out]

Optional. A pointer to a null-terminated string that contains the dotted OID text string of the server response message.  This is normally the same OID  as that which names the request passed to the server in the <i>Oid</i> parameter. Set to <b>NULL</b> if not used.


### -param ReturnedData [out]

Optional. The arbitrary data returned by the extended operation. If <b>NULL</b>, no data is returned by the server. Set this parameter to <b>NULL</b> if not used.


#### - ld [in]

The session handle.


## -returns



If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



The <b>ldap_extended_operation_s</b> function enables a client to send an extended request (free for all) to an LDAP 3 (or later) server. The functionality is open and the client request can be for any operation.

As a synchronous function, <b>ldap_extended_operation_s</b> returns any response data in the <i>ReturnedOid</i> and <i>ReturnedData</i> fields. When no longer required, free the <i>ReturnedOid</i> string and the <i>ReturnedData</i> buffer by calling 
<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a>.  Because <i>ReturnedData</i> is not a <b>PCHAR</b> data type, it must be explicitly cast when used as an argument of <b>ldap_memfree</b>, such as:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>struct berval *pBV;
ldap_extended_operation_s(......., &amp;pBV);
... 
ldap_memfree( (PCHAR) pBV);</pre>
</td>
</tr>
</table></span></div>
Multithreading: The <b>ldap_extended_operation_s</b> function is thread-safe.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/02dda7c5-9779-4390-9395-aa917fa82546">ldap_extended_operation</a>



<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a>
 

 

