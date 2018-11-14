---
UID: NF:fsrmpipeline.IFsrmClassifierModuleImplementation.UseRulesAndDefinitions
title: IFsrmClassifierModuleImplementation::UseRulesAndDefinitions
author: windows-sdk-content
description: Specifies the collection of rules and relevant property definitions the classifier should expect to process.
old-location: fsrm\ifsrmclassifiermoduleimplementation_userulesanddefinitions.htm
tech.root: Fsrm
ms.assetid: 8fbca8c4-7021-4183-b8f7-a32082da17fc
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFsrmClassifierModuleImplementation interface [File Server Resource Manager],UseRulesAndDefinitions method, IFsrmClassifierModuleImplementation.UseRulesAndDefinitions, IFsrmClassifierModuleImplementation::UseRulesAndDefinitions, UseRulesAndDefinitions, UseRulesAndDefinitions method [File Server Resource Manager], UseRulesAndDefinitions method [File Server Resource Manager],IFsrmClassifierModuleImplementation interface, fs.ifsrmclassifiermoduleimplementation_userulesanddefinitions, fsrm.ifsrmclassifiermoduleimplementation_userulesanddefinitions, fsrmpipeline/IFsrmClassifierModuleImplementation::UseRulesAndDefinitions
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFsrmClassifierModuleImplementation.UseRulesAndDefinitions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- fsrmpipeline.h
: 
- IFsrmClassifierModuleImplementation.UseRulesAndDefinitions
: 
---

# IFsrmClassifierModuleImplementation::UseRulesAndDefinitions


## -description


Specifies the collection of rules and relevant property definitions the classifier should expect to 
    process.


## -parameters




### -param rules [in]

Type: <b><a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a>*</b>

An <a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a> instance representing a collection 
       of rules that will be used during the current classification session.


### -param propertyDefinitions [in]

Type: <b><a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a>*</b>

An <a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a> instance representing a collection 
       of property definitions that are referenced by the specified collection of rules.


## -returns



Type: <b>HRESULT</b>

The method returns the following return values.

Other values will result in the client application receiving a 
         <b>FSRM_E_MODULE_SESSION_INITIALIZATION</b> error.

<b>Windows Server 2008 R2:  </b>The client application will receive a <b>FSRM_E_UNEXPECTED</b> error.




## -see-also




<a href="https://msdn.microsoft.com/f238c446-b268-4600-b6e3-ec772a5f7575">IFsrmClassifierModuleImplementation</a>



<a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a>
 

 

