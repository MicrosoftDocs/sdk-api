---
UID: NN:fsrmpipeline.IFsrmClassifierModuleDefinition
title: IFsrmClassifierModuleDefinition
author: windows-sdk-content
description: Defines a classifier module.
old-location: fsrm\ifsrmclassifiermoduledefinition.htm
tech.root: Fsrm
ms.assetid: 6e691670-d7d7-48cb-8a81-ee8828b39b30
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFsrmClassifierModuleDefinition, IFsrmClassifierModuleDefinition interface [File Server Resource Manager], IFsrmClassifierModuleDefinition interface [File Server Resource Manager],described, fs.ifsrmclassifiermoduledefinition, fsrm.ifsrmclassifiermoduledefinition, fsrm/IFsrmClassifierModuleDefinition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
req.dll: SrmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmClassifierModuleDefinition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmClassifierModuleDefinition interface


## -description


Defines a classifier module.

To create a classifier module definition, call the <a href="https://msdn.microsoft.com/1964f4b6-b4e0-45a2-aca1-2e3dc44745a4">IFsrmClassificationManager::CreateModuleDefinition</a> method.

The following methods can return this interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/eeda0802-e450-4a8b-a08c-135784540b17">IFsrmClassificationManager::EnumModuleDefinitions</a>
</li>
<li>
<a href="https://msdn.microsoft.com/41272218-25af-4c8f-8730-37a08a7fad4f">IFsrmClassificationManager::GetModuleDefinition</a>
</li>
</ul>

## -see-also




<a href="https://msdn.microsoft.com/982c82a4-466d-476e-ad17-8f6f1c309c79">IFsrmPipelineModuleDefinition</a>



<a href="https://msdn.microsoft.com/68ecb5e6-61b0-488f-b6bb-181f253de70e">IFsrmStorageModuleDefinition</a>
 

 

