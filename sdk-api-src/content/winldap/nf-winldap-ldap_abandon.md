---
UID: NF:winldap.ldap_abandon
title: ldap_abandon function
author: windows-sdk-content
description: A client calls ldap_abandon to cancel an in-process asynchronous LDAP call.
old-location: ldap\ldap_abandon.htm
old-project: LDAP
ms.assetid: 5c238d98-77f5-4702-bae1-80cdec70a30c
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: "_ldap_ldap_abandon, ldap.ldap__abandon, ldap.ldap_abandon, ldap_abandon, ldap_abandon function [LDAP], winldap/ldap_abandon"
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
tech.root: 
req.typenames: VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, *PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ldap_abandon
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_abandon function


## -description


A client calls <b>ldap_abandon</b> to cancel an in-process asynchronous LDAP call.


## -parameters




### -param ld [in]

The session handle.


### -param msgid [in]

The message ID of the call to be canceled. Asynchronous functions, such as <a href="https://msdn.microsoft.com/fe0d782b-8faf-4666-a952-e2bfd33f6d67">ldap_search</a> and <a href="https://msdn.microsoft.com/93ae0af4-1b16-4bb0-952f-139241189d79">ldap_modify</a>,  return this message ID when they initiate an operation.


## -returns



If the function succeeds, that is, if the cancel operation is successful, the return value is zero.

If the function fails, the return value is –1.




## -remarks



The <b>ldap_abandon</b> function first verifies that the operation has been completed. If it has, the message ID is deleted; otherwise, the call goes to the server to cancel the operation. Be aware that a successful call to <b>ldap_abandon</b> destroys the message ID. Therefore, you cannot call 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> to obtain results with that message ID, even if the server completed the operation.

There is no server response to <b>ldap_abandon</b>; thus, there is no guarantee that the call reached the server.

Multithreading: Calls to <b>ldap_abandon</b> are thread-safe.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>
 

 

