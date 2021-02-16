---
UID: NF:fsrmpipeline.IFsrmClassificationManager.EnumRules
title: IFsrmClassificationManager::EnumRules (fsrmpipeline.h)
description: Enumerates the rules of the specified type.
helpviewer_keywords: ["EnumRules","EnumRules method [File Server Resource Manager]","EnumRules method [File Server Resource Manager]","FsrmClassificationManager class","EnumRules method [File Server Resource Manager]","IFsrmClassificationManager interface","EnumRules method [File Server Resource Manager]","IFsrmClassificationManager2 interface","FsrmClassificationManager class [File Server Resource Manager]","EnumRules method","IFsrmClassificationManager interface [File Server Resource Manager]","EnumRules method","IFsrmClassificationManager.EnumRules","IFsrmClassificationManager2 interface [File Server Resource Manager]","EnumRules method","IFsrmClassificationManager2::EnumRules","IFsrmClassificationManager::EnumRules","fs.ifsrmclassificationmanager_enumrules","fsrm.ifsrmclassificationmanager_enumrules","fsrmpipeline/IFsrmClassificationManager2::EnumRules","fsrmpipeline/IFsrmClassificationManager::EnumRules"]
old-location: fsrm\ifsrmclassificationmanager_enumrules.htm
tech.root: fsrm
ms.assetid: 2f67527c-cde3-4907-9e61-4d9e18b18859
ms.date: 12/05/2018
ms.keywords: EnumRules, EnumRules method [File Server Resource Manager], EnumRules method [File Server Resource Manager],FsrmClassificationManager class, EnumRules method [File Server Resource Manager],IFsrmClassificationManager interface, EnumRules method [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],EnumRules method, IFsrmClassificationManager interface [File Server Resource Manager],EnumRules method, IFsrmClassificationManager.EnumRules, IFsrmClassificationManager2 interface [File Server Resource Manager],EnumRules method, IFsrmClassificationManager2::EnumRules, IFsrmClassificationManager::EnumRules, fs.ifsrmclassificationmanager_enumrules, fsrm.ifsrmclassificationmanager_enumrules, fsrmpipeline/IFsrmClassificationManager2::EnumRules, fsrmpipeline/IFsrmClassificationManager::EnumRules
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
 - IFsrmClassificationManager::EnumRules
 - fsrmpipeline/IFsrmClassificationManager::EnumRules
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
 - IFsrmClassificationManager.EnumRules
 - IFsrmClassificationManager2.EnumRules
 - FsrmClassificationManager.EnumRules
---

# IFsrmClassificationManager::EnumRules


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

Enumerates the rules of the specified type.

## -parameters

### -param ruleType [in]

The type of rules to enumerate. For possible values, see the 
       <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmruletype">FsrmRuleType</a> enumeration.

<div class="alert"><b>Note</b>  The <b>FsrmRuleType_Generic</b> type is not a valid type for this method.</div>
<div> </div>

### -param options [in]

One or more options for enumerating the property definitions. For possible values, see the 
       <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmenumoptions">FsrmEnumOptions</a> enumeration.

<div class="alert"><b>Note</b>  The <b>FsrmEnumOptions_Asynchronous</b> option is not supported for this 
       method.</div>
<div> </div>

### -param Rules [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a> interface that contains a 
       collection of classification rules. Each item in the collection is a <b>VARIANT</b> of 
       type <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant 
       for the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmrule">IFsrmRule</a> interface. You can then use the 
       <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmrule-get_ruletype">IFsrmRule.RuleType</a> property to determine the rule's 
       type. Query the <b>IFsrmRule</b> interface for the rule interface to 
       use. For example, if <b>RuleType</b> is 
       <b>FsrmRuleType_Classification</b>, query the 
       <b>IFsrmRule</b> interface for the 
       <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationrule">IFsrmClassificationRule</a> interface.

The collection contains only committed rules; the collection will not contain newly created rules that have 
       not been committed.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createrule">IFsrmClassificationManager::CreateRule</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getrule">IFsrmClassificationManager::GetRule</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>