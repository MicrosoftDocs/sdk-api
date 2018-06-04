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

# IVssExpressWriter::CreateMetadata


## -description


Creates an express writer metadata object and returns an <a href="https://msdn.microsoft.com/49112cff-9e61-4218-a013-5ae5eb58b534">IVssCreateExpressWriterMetadata</a> interface pointer to it.


## -parameters




### -param writerId [in]

The globally unique identifier (GUID) of the writer class.


### -param writerName [in]

A null-terminated wide character string that contains the name of the writer class. This string is not localized.


### -param usageType [in]

A <a href="https://msdn.microsoft.com/31997417-d993-4f28-b108-ce1dd8239650">VSS_USAGE_TYPE</a> enumeration value that indicates how the data that is managed by the writer is used on the host system. The only valid values for this parameter are VSS_UT_BOOTABLESYSTEMSTATE, VSS_UT_SYSTEMSERVICE, and VSS_UT_USERDATA.


### -param versionMajor [in]

The major version of the writer application. For more information, see the Remarks section.


### -param versionMinor [in]

The minor version of the writer application. For more information, see the Remarks section.


### -param reserved [in]

This parameter is reserved for system use.


### -param ppMetadata [out]

A pointer to a variable that receives an <a href="https://msdn.microsoft.com/49112cff-9e61-4218-a013-5ae5eb58b534">IVssCreateExpressWriterMetadata</a> interface pointer to the newly created express writer metadata.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <i>versionMajor</i> and <i>versionMajor</i> parameters are used to specify the writer's major and minor version numbers according to the following VSS conventions:

<ul>
<li>A writer's minor version number should be incremented by one whenever a released version of the writer contains minor changes that affect the writer's interaction with requesters. For example, a correction to a file specification in a writer QFE or service pack would justify incrementing the minor version number. However, a change between beta or release candidate versions of a writer would not justify the changing of the minor version number.</li>
<li>A writer's major version number should be incremented by one whenever a released version of the writer contains a significant change. For example, if data that is backed up with a new version of a writer cannot be restored using the previous version of the writer, the new writer's major version number should be incremented.</li>
<li>Whenever the major version number is incremented, the minor version number should be reset to zero.</li>
</ul>
If a writer does not specify a version number, VSS will assign a default version number of 0.0.




## -see-also




<a href="https://msdn.microsoft.com/c24a1046-50b0-4fec-88f9-3bbd6970982a">CreateVssExpressWriter</a>



<a href="https://msdn.microsoft.com/debb0731-6e24-4320-8236-220e07ec37c3">IVssExpressWriter</a>
 

 

