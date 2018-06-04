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

# _VSS_PROVIDER_TYPE enumeration


## -description


The <b>VSS_PROVIDER_TYPE</b> enumeration specifies 
    the provider type.


## -enum-fields




### -field VSS_PROV_UNKNOWN

The provider type is unknown. 
     

This indicates an error in the application or the VSS service, or that no provider is available.


### -field VSS_PROV_SYSTEM

The default provider that ships with Windows.


### -field VSS_PROV_SOFTWARE

A software provider.


### -field VSS_PROV_HARDWARE

A hardware provider.


### -field VSS_PROV_FILESHARE

A file share provider.

<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>This enumeration value is not supported until Windows 8 and Windows Server 2012.


## -see-also




<a href="https://msdn.microsoft.com/3f79bf84-c7b9-4291-ae3b-7061fe3199e9">IVssBackupComponents::Query</a>



<a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a>



<a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a>



<a href="https://msdn.microsoft.com/e8d70f20-00a9-4cae-a92c-e3f3673a8db3">VSS_OBJECT_UNION</a>



<a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_PROVIDER_PROP</a>



<a href="https://msdn.microsoft.com/cb89c3cc-5a8e-419e-839c-f72a1886eadf">VSS_SOURCE_TYPE</a>
 

 

