---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0011
title: DataManagerSteps (pla.h)
description: Defines the actions that the data manager takes when it runs.
old-location: pla\datamanagersteps.htm
tech.root: PLA
ms.assetid: e647987d-e524-475e-a355-539cb3f04635
ms.date: 12/05/2018
ms.keywords: DataManagerSteps, DataManagerSteps enumeration [PLA], base.datamanagersteps, pla.datamanagersteps, pla/DataManagerSteps, pla/plaCreateHtml, pla/plaCreateReport, pla/plaFolderActions, pla/plaResourceFreeing, pla/plaRunRules, plaCreateHtml, plaCreateReport, plaFolderActions, plaResourceFreeing, plaRunRules
ms.topic: enum
f1_keywords:
- pla/DataManagerSteps
dev_langs:
- c++
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Pla.h
api_name:
- DataManagerSteps
targetos: Windows
req.typenames: DataManagerSteps
req.redist: 
ms.custom: 19H1
---

# DataManagerSteps enumeration


## -description


Defines the actions that the data manager takes when it runs.


## -enum-fields




### -field plaCreateReport

Runs TraceRpt.exe using as input all the binary performance files (.blg) or event trace files (.etl) in the collection. You can use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_reportschema">IDataManager::ReportSchema</a> property to customize the report.

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_ruletargetfilename">IDataManager::RuleTargetFileName</a> property contains the name of the file that TraceRpt creates.


### -field plaRunRules

If a report exists, apply the rules specified in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_rules">IDataManager::Rules</a> property to the report.

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_ruletargetfilename">RuleTargetFileName</a> property contains the name of the file to which the rules are applied.


### -field plaCreateHtml

Converts the XML file specified in <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_ruletargetfilename">RuleTargetFileName</a> to HTML format. The HTML format is written to the file specified in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_reportfilename">IDataManager::ReportFileName</a> property.


### -field plaFolderActions

Apply the folder actions specified in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_folderactions">IDataManager::FolderActions</a> property to all folders defined in the collection.


### -field plaResourceFreeing

If the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_maxfoldercount">IDataManager::MaxFolderCount</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_maxsize">IDataManager::MaxSize</a>, or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_minfreedisk">IDataManager::MinFreeDisk</a> property exceeds its limit, apply the resource policy specified in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_resourcepolicy">IDataManager::ResourcePolicy</a> property.


## -remarks



Specify one or more actions. The data manager applies the actions in the order in which they are defined in this enumeration.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-run">IDataManager::Run</a>
 

 

