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

# __MIDL_IBackgroundCopyJobHttpOptions_0001 enumeration


## -description


The <b>BG_CERT_STORE_LOCATION</b> enumeration defines the location of the certificate store.


## -enum-fields




### -field BG_CERT_STORE_LOCATION_CURRENT_USER

Use the current user's certificate store.


### -field BG_CERT_STORE_LOCATION_LOCAL_MACHINE

Use the local computer's certificate store.


### -field BG_CERT_STORE_LOCATION_CURRENT_SERVICE

Use the current service's certificate store.


### -field BG_CERT_STORE_LOCATION_SERVICES

Use a specific service's certificate store.


### -field BG_CERT_STORE_LOCATION_USERS

Use a specific user's certificate store.


### -field BG_CERT_STORE_LOCATION_CURRENT_USER_GROUP_POLICY

Use the current user's group policy certificate store. In a network setting, stores in this location are downloaded to the client computer from the Group Policy Template (GPT) during computer startup or user logon. 


### -field BG_CERT_STORE_LOCATION_LOCAL_MACHINE_GROUP_POLICY

Use the local computer's certificate store. In a network setting, stores in this location are downloaded to the client computer from the Group Policy Template (GPT) during computer startup or user logon.


### -field BG_CERT_STORE_LOCATION_LOCAL_MACHINE_ENTERPRISE

Use the enterprise certificate store. The enterprise store is shared across domains in the enterprise and downloaded from the global enterprise directory.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/41fe9366-4c17-43bb-91d6-934c7aa87a2d">System Store Locations</a>.




## -see-also




<a href="https://msdn.microsoft.com/cd317bf9-1d4b-438e-beec-15ea7da90fc9">IBackgroundCopyJobHttpOptions::GetClientCertificate</a>



<a href="https://msdn.microsoft.com/60839bac-7f5f-4c43-84d4-26f1b21f974d">IBackgroundCopyJobHttpOptions::SetClientCertificateByID</a>



<a href="https://msdn.microsoft.com/8262b360-ab05-42a3-b5e7-178dc9f23fc6">IBackgroundCopyJobHttpOptions::SetClientCertificateByName</a>
 

 

