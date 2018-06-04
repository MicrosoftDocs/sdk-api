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

# IFsrmPropertyBag::GetFileStreamInterface


## -description


Retrieves a file stream interface that you can use to access the contents of the file.


## -parameters




### -param accessMode [in]

One or more access modes. For possible values, see the 
      <a href="https://msdn.microsoft.com/a2f7de78-7102-43f9-a7b8-b35ac0b7286a">FsrmFileStreamingMode</a> enumeration.


### -param interfaceType [in]

The type of streaming interface to use. For possible interface types, see the 
      <a href="https://msdn.microsoft.com/182dde15-f8d6-42ab-a9d2-85f0a0a4d670">FsrmFileStreamingInterfaceType</a> 
      enumeration.


### -param pStreamInterface






#### - streamInterface [out]

A <b>VARIANT</b> that contains the streaming interface that you can use to access the 
      contents of the file. The variant is of type <b>VT_DISPATCH</b>. Query the 
      <b>dispval</b> member of the variant to get the specified streaming interface.


## -returns



The method returns the following return values.




## -remarks



To ensure the caller can be authorized for access, it must be a module that has its 
    <a href="https://msdn.microsoft.com/c2cbcfe1-113c-4eb9-9dea-5619bcda58a2">IFsrmPipelineModuleDefinition::NeedsFileContent</a> 
    property set to <b>TRUE</b>. If the <i>accessMode</i> parameter is set to 
    <b>FsrmFileStreamingMode_Write</b>, the caller must also be a storage module and have its 
    <a href="https://msdn.microsoft.com/461befff-0bb4-44a2-9c37-e9a8fb1b080f">IFsrmStorageModuleDefinition::UpdatesFileContent</a> 
    property set to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/237f024d-2b1d-45d5-a63d-c530426278e6">IFsrmPropertyBag</a>
 

 

