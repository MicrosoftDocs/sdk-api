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

# _LSA_OBJECT_ATTRIBUTES structure


## -description


The <b>LSA_OBJECT_ATTRIBUTES</b> structure is used with the 
<a href="https://msdn.microsoft.com/361bc962-1e97-4606-a835-cbce37692c55">LsaOpenPolicy</a> function to specify the attributes of the connection to the <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object.

When you call <a href="https://msdn.microsoft.com/361bc962-1e97-4606-a835-cbce37692c55">LsaOpenPolicy</a>, initialize the members of this structure to <b>NULL</b> or zero because the function does not use the information.


## -struct-fields




### -field Length

Specifies the size, in bytes, of the <b>LSA_OBJECT_ATTRIBUTES</b> structure.


### -field RootDirectory

Should be <b>NULL</b>.


### -field ObjectName

Should be <b>NULL</b>.


### -field Attributes

Should be zero.


### -field SecurityDescriptor

Should be <b>NULL</b>.


### -field SecurityQualityOfService

Should be <b>NULL</b>.


## -remarks



The <b>LSA_OBJECT_ATTRIBUTES</b> structure is defined in the LsaLookup.h header file.

<b>Windows Server 2008 with SP2 and earlier, Windows Vista with SP2 and earlier, Windows Server 2003, Windows XP/2000:  </b>The <b>LSA_OBJECT_ATTRIBUTES</b> structure is defined in the NTSecAPI.h header file.




## -see-also




<a href="https://msdn.microsoft.com/361bc962-1e97-4606-a835-cbce37692c55">LsaOpenPolicy</a>



<a href="https://msdn.microsoft.com/21f99d04-b21b-442c-9034-35f9f7bbee53">SECURITY_QUALITY_OF_SERVICE</a>
 

 

