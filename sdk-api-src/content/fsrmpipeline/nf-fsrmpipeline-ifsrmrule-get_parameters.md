---
UID: NF:fsrmpipeline.IFsrmRule.get_Parameters
title: IFsrmRule::get_Parameters
author: windows-sdk-content
description: The parameters that are passed to the classifier.
old-location: fsrm\ifsrmrule_parameters.htm
tech.root: fsrm
ms.assetid: 8a43763a-15ad-40e2-9e3a-e2c5ca7a7638
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsrmRule interface [File Server Resource Manager],Parameters property, IFsrmRule.Parameters, IFsrmRule.get_Parameters, IFsrmRule::Parameters, IFsrmRule::get_Parameters, IFsrmRule::put_Parameters, Parameters property [File Server Resource Manager], Parameters property [File Server Resource Manager],IFsrmRule interface, fs.ifsrmrule_parameters, fsrm.ifsrmrule_parameters, fsrmpipeline/IFsrmRule::Parameters, fsrmpipeline/IFsrmRule::get_Parameters, fsrmpipeline/IFsrmRule::put_Parameters, get_Parameters
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
 - IFsrmRule.Parameters
 - IFsrmRule.get_Parameters
 - IFsrmRule.put_Parameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmRule::get_Parameters


## -description


The parameters that are passed to the classifier.

This property is read/write.


## -parameters


## -remarks



Specify parameters only if the classifier expects the rule to pass parameters.

The parameters are not passed directly to the classifier. Instead the rule is passed to the classifier which contains the parameters (see the <a href="https://msdn.microsoft.com/69d848b9-4143-4b6c-9a45-66ff44c54b66">IFsrmPipelineModuleImplementation::OnLoad</a> method).

FSRM does not limit the length of the parameter name or value, nor does it limit the number of parameters that you can specify. Specifying a parameter without a value is valid (for example, "parameter=").




## -see-also




<a href="https://msdn.microsoft.com/e1de871f-a2c9-4787-a3e8-8c3428e9249e">IFsrmRule</a>
 

 

