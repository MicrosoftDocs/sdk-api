---
UID: NF:fsrmpipeline.IFsrmClassificationManager.SetFileProperty
title: IFsrmClassificationManager::SetFileProperty
author: windows-sdk-content
description: Sets the value of the specified property in the file or folder.
old-location: fsrm\ifsrmclassificationmanager_setfileproperty.htm
tech.root: fsrm
ms.assetid: 0f13f00e-6ca2-4436-822e-01eff638c446
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FsrmClassificationManager class [File Server Resource Manager],SetFileProperty method, IFsrmClassificationManager interface [File Server Resource Manager],SetFileProperty method, IFsrmClassificationManager.SetFileProperty, IFsrmClassificationManager2 interface [File Server Resource Manager],SetFileProperty method, IFsrmClassificationManager2::SetFileProperty, IFsrmClassificationManager::SetFileProperty, SetFileProperty, SetFileProperty method [File Server Resource Manager], SetFileProperty method [File Server Resource Manager],FsrmClassificationManager class, SetFileProperty method [File Server Resource Manager],IFsrmClassificationManager interface, SetFileProperty method [File Server Resource Manager],IFsrmClassificationManager2 interface, fs.ifsrmclassificationmanager_setfileproperty, fsrm.ifsrmclassificationmanager_setfileproperty, fsrmpipeline/IFsrmClassificationManager2::SetFileProperty, fsrmpipeline/IFsrmClassificationManager::SetFileProperty
ms.topic: method
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
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
 - IFsrmClassificationManager.SetFileProperty
 - IFsrmClassificationManager2.SetFileProperty
 - FsrmClassificationManager.SetFileProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmClassificationManager::SetFileProperty


## -description


Sets the value of the specified property in the file or folder.

<b>Windows Server 2008 R2:  </b>Only files are supported until Windows Server 2012.


## -parameters




### -param filePath [in]

The file that contains the property that you want to set. You must specify an absolute path to the file. You 
      cannot specify a file share.


### -param propertyName [in]

The name of the property whose value you want to set.


### -param propertyValue [in]

The value to set the specified property to.


## -returns



The method returns the following return values.




## -remarks



The method verifies that the property value is valid for the property's type. For example, for an ordered or 
    multiple choice list, that the value is a member of the list; for a Boolean property, that the value is the string 
    "0" or "1"; and for a date, that the value is a 64-bit decimal value expressed 
    as a string.

<b>SetFileProperty</b> only 
    supports property definitions that are available on the server whose 
    <a href="https://msdn.microsoft.com/baa7e2a0-71d3-465e-a4aa-5908b28db703">AppliesTo</a> property has the 
    <b>FsrmPropertyDefinitionAppliesTo_Files</b> (1) bit set.


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



<a href="https://msdn.microsoft.com/c8a3c4cb-4753-495b-88f4-2d6cdfef7dc7">IFsrmClassificationManager::GetFileProperty</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

