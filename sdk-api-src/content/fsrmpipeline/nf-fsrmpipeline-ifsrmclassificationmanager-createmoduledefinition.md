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

# IFsrmClassificationManager::CreateModuleDefinition


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

Creates a module definition of the specified type.


## -parameters




### -param moduleType [in]

The type of module to create (for example, a classifier or storage module). For possible types, see the 
      <a href="https://msdn.microsoft.com/a482c371-a01c-486b-b25b-d22283dba652">FsrmPipelineModuleType</a> enumeration.


### -param moduleDefinition [out]

An <a href="https://msdn.microsoft.com/982c82a4-466d-476e-ad17-8f6f1c309c79">IFsrmPipelineModuleDefinition</a> 
       interface to the new module definition. Query the 
       <b>IFsrmPipelineModuleDefinition</b> interface to 
       get the interface for the specified module. For example, if <i>moduleType</i> is 
       <b>FsrmPipelineModuleType_Classifier</b>, query the 
       <b>IFsrmPipelineModuleDefinition</b> interface 
       for the <a href="https://msdn.microsoft.com/6e691670-d7d7-48cb-8a81-ee8828b39b30">IFsrmClassifierModuleDefinition</a> 
       interface.

To save the module definition, call 
       <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmPipelineModuleDefinition::Commit</a> method.


## -returns



The method returns the following return values.




## -remarks



There is no limit to the number of modules that you can define.

In addition to defining the module with FSRM, you must also register the class with COM. This needs to be a 
    registration of a COM class that implements 
    <a href="https://msdn.microsoft.com/f238c446-b268-4600-b6e3-ec772a5f7575">IFsrmClassifierModuleImplementation</a> or 
    <a href="https://msdn.microsoft.com/8540f1f4-8ed1-4e4d-b940-3e232eb8c2d6">IFsrmStorageModuleImplementation</a>, 
    depending on the type of module.

FSRM provides the following built-in classifiers: the Folder Classifier and the Content Classifier. The Folder 
    Classifier classifies files based on the folder in which they are stored. The Content Classifier classifies by 
    searching for strings and regular expressions in the file using Windows text extraction methods.

FSRM provides the following three built-in storage modules:

<ul>
<li>System Cache Storage Module—stores properties in an NTFS Alternate Data Stream 
      cache.</li>
<li>Office 97 - 2003 In-File Storage Module—stores properties within a Microsoft Office 
      97 - 2003 file.</li>
<li>Office 2007 In-File Storage Module—stores properties within a Microsoft Office 
      2007 (or later) file.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/eeda0802-e450-4a8b-a08c-135784540b17">IFsrmClassificationManager::EnumModuleDefinitions</a>



<a href="https://msdn.microsoft.com/41272218-25af-4c8f-8730-37a08a7fad4f">IFsrmClassificationManager::GetModuleDefinition</a>



<a href="https://msdn.microsoft.com/6e691670-d7d7-48cb-8a81-ee8828b39b30">IFsrmClassifierModuleDefinition</a>



<a href="https://msdn.microsoft.com/4ac8ecc7-a02e-46ce-ac95-35a7dd38e631">IFsrmPipelineModuleConnector::Bind</a>



<a href="https://msdn.microsoft.com/68ecb5e6-61b0-488f-b6bb-181f253de70e">IFsrmStorageModuleDefinition</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

