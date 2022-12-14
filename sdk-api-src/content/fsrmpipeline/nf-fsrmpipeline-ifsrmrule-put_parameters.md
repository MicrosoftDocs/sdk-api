---
UID: NF:fsrmpipeline.IFsrmRule.put_Parameters
title: IFsrmRule::put_Parameters (fsrmpipeline.h)
description: The parameters that are passed to the classifier. (Put)
helpviewer_keywords: ["IFsrmRule interface [File Server Resource Manager]","Parameters property","IFsrmRule.Parameters","IFsrmRule.put_Parameters","IFsrmRule::Parameters","IFsrmRule::get_Parameters","IFsrmRule::put_Parameters","Parameters property [File Server Resource Manager]","Parameters property [File Server Resource Manager]","IFsrmRule interface","fs.ifsrmrule_parameters","fsrm.ifsrmrule_parameters","fsrmpipeline/IFsrmRule::Parameters","fsrmpipeline/IFsrmRule::get_Parameters","fsrmpipeline/IFsrmRule::put_Parameters","put_Parameters"]
old-location: fsrm\ifsrmrule_parameters.htm
tech.root: fsrm
ms.assetid: 8a43763a-15ad-40e2-9e3a-e2c5ca7a7638
ms.date: 12/05/2018
ms.keywords: IFsrmRule interface [File Server Resource Manager],Parameters property, IFsrmRule.Parameters, IFsrmRule.put_Parameters, IFsrmRule::Parameters, IFsrmRule::get_Parameters, IFsrmRule::put_Parameters, Parameters property [File Server Resource Manager], Parameters property [File Server Resource Manager],IFsrmRule interface, fs.ifsrmrule_parameters, fsrm.ifsrmrule_parameters, fsrmpipeline/IFsrmRule::Parameters, fsrmpipeline/IFsrmRule::get_Parameters, fsrmpipeline/IFsrmRule::put_Parameters, put_Parameters
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmRule::put_Parameters
 - fsrmpipeline/IFsrmRule::put_Parameters
dev_langs:
 - c++
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
---

# IFsrmRule::put_Parameters


## -description

The parameters that are passed to the classifier.

This property is read/write.

## -parameters

## -remarks

Specify parameters only if the classifier expects the rule to pass parameters.

The parameters are not passed directly to the classifier. Instead the rule is passed to the classifier which contains the parameters (see the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduleimplementation-onload">IFsrmPipelineModuleImplementation::OnLoad</a> method).

FSRM does not limit the length of the parameter name or value, nor does it limit the number of parameters that you can specify. Specifying a parameter without a value is valid (for example, "parameter=").

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmrule">IFsrmRule</a>
