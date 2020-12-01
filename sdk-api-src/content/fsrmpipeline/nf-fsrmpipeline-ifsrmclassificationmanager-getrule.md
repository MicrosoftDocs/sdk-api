---
UID: NF:fsrmpipeline.IFsrmClassificationManager.GetRule
title: IFsrmClassificationManager::GetRule (fsrmpipeline.h)
description: Retrieves the specified rule.
helpviewer_keywords: ["FsrmClassificationManager class [File Server Resource Manager]","GetRule method","GetRule","GetRule method [File Server Resource Manager]","GetRule method [File Server Resource Manager]","FsrmClassificationManager class","GetRule method [File Server Resource Manager]","IFsrmClassificationManager interface","GetRule method [File Server Resource Manager]","IFsrmClassificationManager2 interface","IFsrmClassificationManager interface [File Server Resource Manager]","GetRule method","IFsrmClassificationManager.GetRule","IFsrmClassificationManager2 interface [File Server Resource Manager]","GetRule method","IFsrmClassificationManager2::GetRule","IFsrmClassificationManager::GetRule","fs.ifsrmclassificationmanager_getrule","fsrm.ifsrmclassificationmanager_getrule","fsrmpipeline/IFsrmClassificationManager2::GetRule","fsrmpipeline/IFsrmClassificationManager::GetRule"]
old-location: fsrm\ifsrmclassificationmanager_getrule.htm
tech.root: fsrm
ms.assetid: 2c21ed09-6c69-4f03-91bb-9beeb816ed62
ms.date: 12/05/2018
ms.keywords: FsrmClassificationManager class [File Server Resource Manager],GetRule method, GetRule, GetRule method [File Server Resource Manager], GetRule method [File Server Resource Manager],FsrmClassificationManager class, GetRule method [File Server Resource Manager],IFsrmClassificationManager interface, GetRule method [File Server Resource Manager],IFsrmClassificationManager2 interface, IFsrmClassificationManager interface [File Server Resource Manager],GetRule method, IFsrmClassificationManager.GetRule, IFsrmClassificationManager2 interface [File Server Resource Manager],GetRule method, IFsrmClassificationManager2::GetRule, IFsrmClassificationManager::GetRule, fs.ifsrmclassificationmanager_getrule, fsrm.ifsrmclassificationmanager_getrule, fsrmpipeline/IFsrmClassificationManager2::GetRule, fsrmpipeline/IFsrmClassificationManager::GetRule
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmTlb.h
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
 - IFsrmClassificationManager::GetRule
 - fsrmpipeline/IFsrmClassificationManager::GetRule
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
 - IFsrmClassificationManager.GetRule
 - IFsrmClassificationManager2.GetRule
 - FsrmClassificationManager.GetRule
---

# IFsrmClassificationManager::GetRule


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

Retrieves the specified rule.

## -parameters

### -param ruleName [in]

The name of the rule to retrieve. Must not exceed 100 characters in length.

### -param ruleType [in]

The type of the rule to retrieve. For possible types, see the 
       <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmruletype">FsrmRuleType</a> enumeration.

<div class="alert"><b>Note</b>  The <b>FsrmRuleType_Generic</b> type is not supported by this method.</div>
<div> </div>

### -param Rule [out]

An <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmrule">IFsrmRule</a> interface to  the retrieved rule. Query the 
      <b>IFsrmRule</b> interface to get the interface for the specified 
      type. For example, if <i>ruleType</i> is 
      <b>FsrmRuleType_Classification</b>, query the 
      <b>IFsrmRule</b> interface for the 
      <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationrule">IFsrmClassificationRule</a> interface.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createrule">IFsrmClassificationManager::CreateRule</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumrules">IFsrmClassificationManager::EnumRules</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>