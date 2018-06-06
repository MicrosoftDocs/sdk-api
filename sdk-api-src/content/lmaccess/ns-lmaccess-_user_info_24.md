---
UID: NS:lmaccess._USER_INFO_24
title: "_USER_INFO_24"
author: windows-sdk-content
description: Contains user account information on an account which is connected to an Internet identity. This information includes the Internet provider name for the user, the user's Internet name, and the user's security identifier (SID).
old-location: netmgmt\user_info_24.htm
old-project: NetMgmt
ms.assetid: CE65EDE0-F4AE-4582-9D7F-6667BBA98C75
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*LPUSER_INFO_24, *PUSER_INFO_24, LPUSER_INFO_24, LPUSER_INFO_24 structure pointer [Network Management], PUSER_INFO_24, PUSER_INFO_24 structure pointer [Network Management], USER_INFO_24, USER_INFO_24 structure [Network Management], _USER_INFO_24, lmaccess/LPUSER_INFO_24, lmaccess/PUSER_INFO_24, lmaccess/USER_INFO_24, netmgmt.user_info_24"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lmaccess.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: USER_INFO_24, *PUSER_INFO_24, *LPUSER_INFO_24
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - USER_INFO_24
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _USER_INFO_24 structure


## -description


The
				<b>USER_INFO_24</b> structure contains user account information on an account which is connected to an Internet identity. This information includes the Internet provider name for the user, the user's Internet name, and the user's security identifier (SID).


## -struct-fields




### -field usri24_internet_identity

A boolean value that indicates whether an account is connected to an Internet identity. 

This member is true if the account is connected  to an Internet identity. The other members in this structure can be used. 

If this member is false, then the account is not connected  to an Internet identity and other members in this structure should be ignored.


### -field usri24_flags

A set of flags. This member must be zero.


### -field usri24_internet_provider_name

A pointer to a Unicode string that specifies the Internet provider name. 


### -field usri24_internet_principal_name

A pointer to a Unicode string that specifies the user's Internet name. 


### -field usri24_user_sid

The local account SID of the user.


## -remarks



A user's account for logging onto Windows can be connected to an Internet identity. The user account can be a local account on a computer or a domain account for computers joined to a domain. The <b>USER_INFO_24</b> structure is used to provide information on an account which is connected to an Internet identity.

On Windows 8 and Windows Server 2012, the Internet identity for a connected account can often be used instead of the computer account.




## -see-also




<a href="https://msdn.microsoft.com/5bd13bed-938a-4273-840e-99fca99f7139">NetUserGetInfo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>
 

 

