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

# SendToMode enumeration


## -description


Defines the way a file will be faxed from within an application. With Windows Vista there is only one possible value.


## -enum-fields




### -field SEND_TO_FAX_RECIPIENT_ATTACHMENT

The file is faxed as it is. The user cannot add typed material preceding it or following it.


## -remarks



This enumeration is used primarily as a parameter for the <a href="https://msdn.microsoft.com/19ab50a4-a2fb-40be-a9e8-e29d149bb274">SendToFaxRecipient</a> function. 




## -see-also




<a href="https://msdn.microsoft.com/19ab50a4-a2fb-40be-a9e8-e29d149bb274">SendToFaxRecipient</a>



<a href="https://msdn.microsoft.com/555ee494-ee1c-4047-b7ae-a890176a6b32">Shell Fax Extension Functions</a>
 

 

