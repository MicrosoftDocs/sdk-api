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

# IFsrmExportImport::ExportQuotaTemplates


## -description


Exports one or more quota templates to the specified file.


## -parameters




### -param filePath [in]

The full path to the export file that will contain the quota templates in XML format. The string is limited 
      to 260 characters.


### -param templateNamesSafeArray [in]

A variant that contains the names of the quota templates to export. Set the variant to empty or 
       <b>NULL</b> to export all templates.

Set the variant type to both <b>VT_ARRAY</b> and <b>VT_VARIANT</b> and 
       the <b>parray</b> member to the <b>SAFEARRAY</b> of 
       <b>BSTR</b>s.


### -param remoteHost [in]

The name of the remote server. To specify the local server, set to an empty string.


## -returns



This method can return the following error codes.




## -remarks



The quota template name is specified when you call the 
    <a href="https://msdn.microsoft.com/d8dbc0fb-de02-4491-94f5-e845a2338251">IFsrmQuotaTemplateManager::CreateTemplate</a> 
    method. To enumerate the templates, call the 
    <a href="https://msdn.microsoft.com/e5f5b94a-6b17-4379-9141-07ec70a830e9">IFsrmQuotaTemplateManager::EnumTemplates</a> 
    method.

You can also use the 
    <a href="https://msdn.microsoft.com/36ba071b-4db2-42fb-90a8-838c45dfdd16">IFsrmQuotaTemplateManager::ExportTemplates</a> 
    method to export the templates.




## -see-also




<a href="https://msdn.microsoft.com/ea707982-2d2d-4fb9-a97a-ee5b2a61f8a9">FsrmExportImport</a>



<a href="https://msdn.microsoft.com/5a3b682e-d2c3-43b3-9d10-4bba9d9c81d4">IFsrmExportImport</a>
 

 

