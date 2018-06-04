---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _WLX_MPR_NOTIFY_INFO structure


## -description


<p class="CCE_Message">[The WLX_MPR_NOTIFY_INFO structure is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WLX_MPR_NOTIFY_INFO</b> structure provides identification and authentication information to network providers.

 Your <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL returns this information to Winlogon following a successful authentication. <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a> is responsible for freeing both the main structure and all strings pointed to from within the structure.


## -struct-fields




### -field pszUserName

A pointer to the name of the account logged onto (for example "user_name"). 




The string pointed to by <b>pszUserName</b> must be separately allocated by your GINA DLL. It will be deallocated by Winlogon.


### -field pszDomain

A pointer to the name of the domain used to log on. 




The string pointed to by pszDomain must be separately allocated by your GINA DLL. It will be deallocated by Winlogon.


### -field pszPassword

A pointer to the plaintext password of the user account. If <b>pszOldPassword</b> is not <b>NULL</b>, <b>pszPassword</b> contains the new password from a password-change operation. 




The string pointed to by <b>pszPassword</b> must be separately allocated by your GINA DLL. It will be deallocated by Winlogon.

 For information about protecting passwords, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.
					


### -field pszOldPassword

A pointer to the plaintext old password of the user account whose password has just been changed (in this case, <i>pszPassword</i> contains the new password). 




The string pointed to by <b>pszOldPassword</b> must be separately allocated by your GINA DLL. It will be deallocated by Winlogon.

