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

# VSS_USAGE_TYPE enumeration


## -description


The <b>VSS_USAGE_TYPE</b> enumeration specifies how 
    the host system uses the data managed by a writer involved in a VSS operation.


## -enum-fields




### -field VSS_UT_UNDEFINED

The usage type is not known. 
      

This indicates an error on the part of the writer.


### -field VSS_UT_BOOTABLESYSTEMSTATE

The data stored by the writer is part of the bootable system state.


### -field VSS_UT_SYSTEMSERVICE

The writer either stores data used by a system service or is a system service itself.


### -field VSS_UT_USERDATA

The data is user data.


### -field VSS_UT_OTHER

Unclassified data.


## -remarks



The usage type of the data that a writer manages is specified when it initializes its cooperation with the 
    shadow copy mechanism through 
    <a href="https://msdn.microsoft.com/a427ebbd-b7c4-46ba-ba16-dd601b1f956e">CVssWriter::Initialize</a>.

Information about the usage type of the data that a writer manages can be retrieved through its metadata using 
    <a href="https://msdn.microsoft.com/55240ef2-f480-4917-98f9-e88a2e23edea">IVssExamineWriterMetadata::GetIdentity</a>.

Requester applications that are interested in backing up system state should look for writers with the  <b>VSS_UT_BOOTABLESYSTEMSTATE</b> or  <b>VSS_UT_SYSTEMSERVICE</b> usage type.




## -see-also




<a href="https://msdn.microsoft.com/a427ebbd-b7c4-46ba-ba16-dd601b1f956e">CVssWriter::Initialize</a>



<a href="https://msdn.microsoft.com/55240ef2-f480-4917-98f9-e88a2e23edea">IVssExamineWriterMetadata::GetIdentity</a>



<a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a>



<a href="https://msdn.microsoft.com/b7c91003-0ce7-463e-a816-c212da9dc31e">VSS_OBJECT_TYPE</a>



<a href="https://msdn.microsoft.com/cb89c3cc-5a8e-419e-839c-f72a1886eadf">VSS_SOURCE_TYPE</a>
 

 

