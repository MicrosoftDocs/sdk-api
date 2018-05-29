---
UID: NF:fsrmpipeline.IFsrmPipelineModuleDefinition.put_NeedsFileContent
title: IFsrmPipelineModuleDefinition::put_NeedsFileContent
author: windows-sdk-content
description: Determines whether the module needs to read the contents of the file.
old-location: fsrm\ifsrmpipelinemoduledefinition_needsfilecontent.htm
old-project: Fsrm
ms.assetid: c2cbcfe1-113c-4eb9-9dea-5619bcda58a2
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: IFsrmPipelineModuleDefinition interface [File Server Resource Manager],NeedsFileContent property, IFsrmPipelineModuleDefinition.NeedsFileContent, IFsrmPipelineModuleDefinition.put_NeedsFileContent, IFsrmPipelineModuleDefinition::NeedsFileContent, IFsrmPipelineModuleDefinition::get_NeedsFileContent, IFsrmPipelineModuleDefinition::put_NeedsFileContent, NeedsFileContent property [File Server Resource Manager], NeedsFileContent property [File Server Resource Manager],IFsrmPipelineModuleDefinition interface, fs.ifsrmpipelinemoduledefinition_needsfilecontent, fsrm.ifsrmpipelinemoduledefinition_needsfilecontent, fsrmpipeline/IFsrmPipelineModuleDefinition::NeedsFileContent, fsrmpipeline/IFsrmPipelineModuleDefinition::get_NeedsFileContent, fsrmpipeline/IFsrmPipelineModuleDefinition::put_NeedsFileContent, put_NeedsFileContent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmpipeline.h
req.include-header: 
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmPipelineModuleDefinition.NeedsFileContent
-	IFsrmPipelineModuleDefinition.get_NeedsFileContent
-	IFsrmPipelineModuleDefinition.put_NeedsFileContent
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmPipelineModuleDefinition::put_NeedsFileContent


## -description


Determines whether the module needs to read the contents of the file.

This property is read/write.


## -parameters


## -remarks



If the 
    <b>NeedsFileContent</b> property 
    value is <b>VARIANT_TRUE</b>, FSRM will provide a stream for a file's contents to the module. 
    This may be necessary if a classification module needs to analyze the contents of the file to determine the 
    property values or if a storage module handles property values embedded in the file's contents




## -see-also




<a href="https://msdn.microsoft.com/982c82a4-466d-476e-ad17-8f6f1c309c79">IFsrmPipelineModuleDefinition</a>
 

 

