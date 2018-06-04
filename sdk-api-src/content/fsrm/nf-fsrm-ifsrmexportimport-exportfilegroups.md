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

# IFsrmExportImport::ExportFileGroups


## -description


Exports one or more file groups to the specified file.


## -parameters




### -param filePath [in]

The full path to the export file that will contain the file groups in XML format. The string is limited to 
      260 characters.


### -param fileGroupNamesSafeArray [in]

A variant that contains the names of the file groups to export. Set the variant to empty or 
      <b>NULL</b> to export all file groups.

Set the variant type to both 
      <b>VT_ARRAY</b> and <b>VT_VARIANT</b> and the 
      <b>parray</b> member to the <b>SAFEARRAY</b> of 
      <b>BSTR</b>s.


### -param remoteHost [in]

The name of the remote server. To specify the local server, set to an empty string.


## -returns



This method can return the following error codes.




## -remarks



The file group name is specified when you call the 
    <a href="https://msdn.microsoft.com/7e2c3672-fbb9-4da5-9e20-25c66213843c">IFsrmFileGroupManager::CreateFileGroup</a> 
    method. To enumerate the file groups, call the 
    <a href="https://msdn.microsoft.com/317eb6cf-7bcc-4042-a7b7-05efac84a0c2">IFsrmFileGroupManager::EnumFileGroups</a> 
    method.

You can also use the 
    <a href="https://msdn.microsoft.com/59d7ef32-f06b-4167-8e28-da88da27ab0a">IFsrmFileGroupManager::ExportFileGroups</a> 
    method to export the templates.




## -see-also




<a href="https://msdn.microsoft.com/ea707982-2d2d-4fb9-a97a-ee5b2a61f8a9">FsrmExportImport</a>



<a href="https://msdn.microsoft.com/5a3b682e-d2c3-43b3-9d10-4bba9d9c81d4">IFsrmExportImport</a>
 

 

