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

# NETSOURCE_URLCREDPOLICY_SETTINGS enumeration


## -description



The <b>NETSOURCE_URLCREDPOLICY_SETTINGS</b> enumeration type is used for an output parameter of <a href="https://msdn.microsoft.com/5840fe0b-34f6-4e39-b55f-7e07b7795e52">IWMSInternalAdminNetSource2::GetCredentialsEx</a>. It specifies possible security policy settings that can exist on a client computer. When you retrieve credentials, you must proceed as dictated by the user's security preferences. For more information, see <b>GetCredentialsEx</b>.




## -enum-fields




### -field NETSOURCE_URLCREDPOLICY_SETTING_SILENTLOGONOK

Specifies that your application can log on to servers for which passwords are cached without informing the user.


### -field NETSOURCE_URLCREDPOLICY_SETTING_MUSTPROMPTUSER

Specifies that your application must notify the user when your application needs to log on to a server. You application can fill in the fields of a password dialog, but must get confirmation.


### -field NETSOURCE_URLCREDPOLICY_SETTING_ANONYMOUSONLY

Specifies that your application can never log on to network servers for the user. Your application can still navigate servers that do not require passwords.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>
 

 

