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

# VSS_SOURCE_TYPE enumeration


## -description


The <b>VSS_SOURCE_TYPE</b> enumeration specifies the 
    type of data that a writer manages.


## -enum-fields




### -field VSS_ST_UNDEFINED

The source of the data is not known. 
      

This indicates a writer error, and the requester should report it.


### -field VSS_ST_TRANSACTEDDB

The source of the data is a database that supports transactions, such as Microsoft SQL Server.


### -field VSS_ST_NONTRANSACTEDDB

The source of the data is a database that does not support transactions.


### -field VSS_ST_OTHER

Unclassified source type—data will be in a file group. 
      

This is the default source type.


## -remarks



The source type of the data that a writer manages is specified when it initializes its cooperation with the 
    shadow copy mechanism through a call to 
    <a href="https://msdn.microsoft.com/a427ebbd-b7c4-46ba-ba16-dd601b1f956e">CVssWriter::Initialize</a>.

Information about the source type of the data that a writer manages can be retrieved through its metadata 
    using 
    <a href="https://msdn.microsoft.com/55240ef2-f480-4917-98f9-e88a2e23edea">IVssExamineWriterMetadata::GetIdentity</a>.




## -see-also




<a href="https://msdn.microsoft.com/a427ebbd-b7c4-46ba-ba16-dd601b1f956e">CVssWriter::Initialize</a>



<a href="https://msdn.microsoft.com/55240ef2-f480-4917-98f9-e88a2e23edea">IVssExamineWriterMetadata::GetIdentity</a>



<a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a>



<a href="https://msdn.microsoft.com/b7c91003-0ce7-463e-a816-c212da9dc31e">VSS_OBJECT_TYPE</a>



<a href="https://msdn.microsoft.com/31997417-d993-4f28-b108-ce1dd8239650">VSS_USAGE_TYPE</a>
 

 

