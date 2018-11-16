---
UID: NE:vswriter.VSS_USAGE_TYPE
title: VSS_USAGE_TYPE
author: windows-sdk-content
description: Specifies how the host system uses the data managed by a writer involved in a VSS operation.
old-location: base\vss_usage_type.htm
tech.root: VSS
ms.assetid: 31997417-d993-4f28-b108-ce1dd8239650
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: VSS_USAGE_TYPE, VSS_USAGE_TYPE enumeration [VSS], VSS_UT_BOOTABLESYSTEMSTATE, VSS_UT_OTHER, VSS_UT_SYSTEMSERVICE, VSS_UT_UNDEFINED, VSS_UT_USERDATA, _win32_vss_usage_type, base.vss_usage_type, enumeration [VSS], vswriter/VSS_USAGE_TYPE, vswriter/VSS_UT_BOOTABLESYSTEMSTATE, vswriter/VSS_UT_OTHER, vswriter/VSS_UT_SYSTEMSERVICE, vswriter/VSS_UT_UNDEFINED, vswriter/VSS_UT_USERDATA
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VsWriter.h
api_name:
 - VSS_USAGE_TYPE
product: Windows
targetos: Windows
req.typenames: VSS_USAGE_TYPE
req.redist: 
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
 

 

