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

# __MIDL___MIDL_itf_ads_0001_0048_0006 enumeration


## -description


The <b>ADS_SD_REVISION_ENUM</b> enumeration specifies the revision number of the access-control entry (ACE), or the access-control list (ACL), for Active Directory.


## -enum-fields




### -field ADS_SD_REVISION_DS

The revision number of the ACE, or the ACL, for Active Directory.


## -remarks



The <b>ADS_SD_REVISION_DS</b> flag signifies that the related ACL contains object-specific ACEs.

Because VBScript cannot read data from a type library, VBScript applications cannot recognize the symbolic constants as defined above. Use the numerical constants instead to set the appropriate flags in your VBScript applications. To use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done here, in your VBScript applications.




## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI Enumerations</a>
 

 

