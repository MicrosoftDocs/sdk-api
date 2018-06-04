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

# __MIDL___MIDL_itf_ads_0001_0078_0001 enumeration


## -description


The <b>ADS_SETTYPE_ENUM</b> enumeration specifies the available pathname format used by the  <a href="https://msdn.microsoft.com/1672c1b0-1008-41e7-8ca4-eefb559f523d">IADsPathname::Set</a> method.


## -enum-fields




### -field ADS_SETTYPE_FULL

Sets the full path, for example, "LDAP://servername/o=internet/…/cn=bar".


### -field ADS_SETTYPE_PROVIDER

Updates the provider only, for example, "LDAP".


### -field ADS_SETTYPE_SERVER

Updates the server name only, for example, "servername".


### -field ADS_SETTYPE_DN

Updates the distinguished name only, for example, "o=internet/…/cn=bar".


## -remarks



Since VBScript cannot read information from a type library, VBScript applications do not understand the symbolic constants as defined above. You should use the numerical constants instead to set the appropriate flags in your VBScript applications. If you want to use the symbolic constants as a good programming practice, you should make explicit declarations of such constants, as done here, in your VBScript applications.




## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI Enumerations</a>



<a href="https://msdn.microsoft.com/1672c1b0-1008-41e7-8ca4-eefb559f523d">IADsPathname::Set</a>
 

 

