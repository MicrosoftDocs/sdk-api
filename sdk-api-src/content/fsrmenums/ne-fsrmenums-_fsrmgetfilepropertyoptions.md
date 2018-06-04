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

# _FsrmGetFilePropertyOptions enumeration


## -description


Flags that defines how classification properties associated with a file are retrieved.


## -enum-fields




### -field FsrmGetFilePropertyOptions_None

Retrieve the most up-to-date classification properties. Using this value may require more time than the 
      <b>FsrmGetFilePropertyOptions_NoRuleEvaluation</b> value.


### -field FsrmGetFilePropertyOptions_NoRuleEvaluation

Retrieve classification properties from cache or storage without using any rule evaluation.


### -field FsrmGetFilePropertyOptions_Persistent

After retrieving the classification properties (and possibly reclassifying the file in the process), store 
       the classification properties with the file.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.


### -field FsrmGetFilePropertyOptions_FailOnPersistErrors

If the <b>FsrmGetFilePropertyOptions_Persistent</b> flag is set but the properties were 
       unable to be stored with the file, return a failure for the operation. If this flag is clear the operation will 
       not fail even though the properties were not persisted with the file.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.


### -field FsrmGetFilePropertyOptions_SkipOrphaned

If the <b>FsrmGetFilePropertyOptions_Persistent</b> flag is set, skip any properties 
       stored with the file that are not also defined for the machine.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.


## -see-also




<a href="https://msdn.microsoft.com/93fdf667-8959-40a9-a374-c54ed73bbe89">FSRM Enumerations</a>



<a href="https://msdn.microsoft.com/9a833e94-d26b-4c94-bf2f-76ac6db3f8e9">IFsrmClassificationManager::EnumFileProperties</a>



<a href="https://msdn.microsoft.com/c8a3c4cb-4753-495b-88f4-2d6cdfef7dc7">IFsrmClassificationManager::GetFileProperty</a>
 

 

