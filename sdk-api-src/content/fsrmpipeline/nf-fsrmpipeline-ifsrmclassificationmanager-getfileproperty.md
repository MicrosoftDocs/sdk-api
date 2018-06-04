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

# IFsrmClassificationManager::GetFileProperty


## -description


Retrieves the specified property from the file or folder.

<b>Windows Server 2008 R2:  </b>Only files are supported until Windows Server 2012.


## -parameters




### -param filePath [in]

The file that contains the property that you want to retrieve. You must specify an absolute path to the 
      file. You cannot specify a file share.


### -param propertyName [in]

The name of the property to retrieve. Must not exceed 100 characters in length.


### -param options [in]

The option to use for retrieving the file's property. For possible values, see the 
      <a href="https://msdn.microsoft.com/d909e244-344f-4da9-987c-de406c2dc359">FsrmGetFilePropertyOptions</a> enumeration.


### -param property [out]

An <a href="https://msdn.microsoft.com/feffccd1-cf72-45c0-97b3-d6efd736223e">IFsrmProperty</a> interface to  the retrieved 
      property.


## -returns



The method returns the following return values.




## -remarks



FSRM asks the specified storage modules (see the <i>options</i> parameter) to retrieve the 
    property from the file. If the <i>options</i> parameter is set to 
    <b>FsrmGetFilePropertyOptions_None</b>, FSRM reruns classification on the file to ensure the 
    correct value is returned.


#### Examples

For examples in C# and PowerShell see 
     <a href="https://msdn.microsoft.com/E057898F-72A0-4AB0-BE88-4C1BE6B2B5DE">Accessing Classification Properties</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/bac42416-0757-462f-8869-339655f48587">IFsrmClassificationManager::ClearFileProperty</a>



<a href="https://msdn.microsoft.com/9a833e94-d26b-4c94-bf2f-76ac6db3f8e9">IFsrmClassificationManager::EnumFileProperties</a>



<a href="https://msdn.microsoft.com/0f13f00e-6ca2-4436-822e-01eff638c446">IFsrmClassificationManager::SetFileProperty</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

