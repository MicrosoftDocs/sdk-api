---
UID: NE:vswriter.VSS_SOURCE_TYPE
title: VSS_SOURCE_TYPE
author: windows-sdk-content
description: Specifies the type of data that a writer manages.
old-location: base\vss_source_type.htm
old-project: vss
ms.assetid: cb89c3cc-5a8e-419e-839c-f72a1886eadf
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: VSS_SOURCE_TYPE, VSS_SOURCE_TYPE enumeration [VSS], VSS_ST_NONTRANSACTEDDB, VSS_ST_OTHER, VSS_ST_TRANSACTEDDB, VSS_ST_UNDEFINED, _win32_vss_source_type, base.vss_source_type, enumeration [VSS], vswriter/VSS_SOURCE_TYPE, vswriter/VSS_ST_NONTRANSACTEDDB, vswriter/VSS_ST_OTHER, vswriter/VSS_ST_TRANSACTEDDB, vswriter/VSS_ST_UNDEFINED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vswriter.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VSS_SOURCE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VsWriter.h
api_name:
 - VSS_SOURCE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
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
 

 

