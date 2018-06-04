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

# IBITSExtensionSetupFactory::GetObject


## -description


Use the 
<b>GetObject</b> method to retrieve a pointer to the 
<a href="https://msdn.microsoft.com/840608ef-9c07-43f7-9cfd-20996a18bb50">IBITSExtensionSetup</a> interface. This method performs the same binding that the 
<a href="https://msdn.microsoft.com/595b2c7f-584c-4343-a75c-327d8ed4ceb1">ADsGetObject</a> ADSI function performs.


## -parameters




### -param Path [in]

Null-terminated string containing the path to the directory service. For example, "IIS://&lt;machine name&gt;/w3svc/1/<i>virtual directory</i>".


### -param ppExtensionSetup [out]

Use the 
<a href="https://msdn.microsoft.com/840608ef-9c07-43f7-9cfd-20996a18bb50">IBITSExtensionSetup</a> interface to enable and disable BITS upload for the given virtual directory.


## -returns



This method returns <b>S_OK</b> for success. Otherwise, the method failed.




## -see-also




<a href="https://msdn.microsoft.com/840608ef-9c07-43f7-9cfd-20996a18bb50">IBITSExtensionSetup</a>
 

 

