---
UID: NF:winldap.ldap_extended_operationA
title: ldap_extended_operationA function
author: windows-sdk-content
description: The ldap_extended_operation function enables you to pass extended LDAP operations to the server.
old-location: ldap\ldap_extended_operation.htm
old-project: LDAP
ms.assetid: 02dda7c5-9779-4390-9395-aa917fa82546
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: "_ldap_ldap_extended_operation, ldap.ldap__extended__operation, ldap.ldap_extended_operation, ldap_extended_operation, ldap_extended_operation function [LDAP], ldap_extended_operationA, ldap_extended_operationW, winldap/ldap_extended_operation, winldap/ldap_extended_operationA, winldap/ldap_extended_operationW"
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
req.unicode-ansi: ldap_extended_operationW (Unicode) and ldap_extended_operationA (ANSI)
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
-	ldap_extended_operation
-	ldap_extended_operationA
-	ldap_extended_operationW
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_extended_operationA function


## -description


The <b>ldap_extended_operation</b> function enables you to pass extended LDAP operations to the server.


## -parameters




### -param ld [in]

The session handle.


### -param Oid [in]

A pointer to a null-terminated string that contains the dotted object identifier  text string that names the request.


### -param Data [in]

The arbitrary data required by the operation. If <b>NULL</b>, no data is sent to the server.


### -param ServerControls [in]

Optional. A list of LDAP server controls. Set this parameter to <b>NULL</b>, if not used.


### -param ClientControls [in]

Optional. A list of client controls. Set this parameter to <b>NULL</b>, if not used.


### -param MessageNumber [out]

The message ID for the request.


## -returns



If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



The <b>ldap_extended_operation</b> function enables a client to send an extended request (free for all) to an LDAP 3 (or later) server. The functionality is open and the client request can be for any operation.

As an asynchronous function, <b>ldap_extended_operation</b> returns a message ID for the operation. Call 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous operation, call 
<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>.

Because of the open nature of the request, the client must call 
<a href="https://msdn.microsoft.com/829ffb8f-150b-438a-bcbd-42f2e9c01479">ldap_close_extended_op</a> to terminate the request.

Multithreading: The <b>ldap_extended_operation</b> function is thread-safe.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>



<a href="https://msdn.microsoft.com/829ffb8f-150b-438a-bcbd-42f2e9c01479">ldap_close_extended_op</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>
 

 

