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

# __MIDL___MIDL_itf_ads_0001_0078_0002 enumeration


## -description


The <b>ADS_FORMAT_ENUM</b> enumeration specifies the available path value types used by the  <a href="https://msdn.microsoft.com/c34f2a5e-5faf-45bf-acc6-8db5fc8bf5fa">IADsPathname::Retrieve</a> method.


## -enum-fields




### -field ADS_FORMAT_WINDOWS

Returns the full path in Windows format, for example, "LDAP://servername/o=internet/…/cn=bar".


### -field ADS_FORMAT_WINDOWS_NO_SERVER

Returns Windows format without server, for example, "LDAP://o=internet/…/cn=bar".


### -field ADS_FORMAT_WINDOWS_DN

Returns Windows format of the distinguished name only, for example, "o=internet/…/cn=bar".


### -field ADS_FORMAT_WINDOWS_PARENT

Returns Windows format of Parent only, for example, "o=internet/…".


### -field ADS_FORMAT_X500

Returns the full path in X.500 format, for example, "LDAP://servername/cn=bar,…,o=internet".


### -field ADS_FORMAT_X500_NO_SERVER

Returns the path without server in X.500 format, for example, "LDAP://cn=bar,…,o=internet".


### -field ADS_FORMAT_X500_DN

Returns only the distinguished name in X.500 format. For example, "cn=bar,…,o=internet".


### -field ADS_FORMAT_X500_PARENT

Returns only the parent in X.500 format, for example, "…,o=internet".


### -field ADS_FORMAT_SERVER

Returns the server name, for example, "servername".


### -field ADS_FORMAT_PROVIDER

Returns the name of the provider, for example, "LDAP".


### -field ADS_FORMAT_LEAF

Returns the name of the leaf, for example, "cn=bar".


## -remarks



The WinNT provider does not support any of the X.500 format specifiers.

Because Visual Basic Scripting Edition  cannot read data from a type library, VBScript applications cannot recognize the symbolic constants as defined above. You should use the numeric constants instead to set the appropriate flags in your VBScript applications. To use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done here.




## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI Enumerations</a>



<a href="https://msdn.microsoft.com/c34f2a5e-5faf-45bf-acc6-8db5fc8bf5fa">IADsPathname::Retrieve</a>
 

 

