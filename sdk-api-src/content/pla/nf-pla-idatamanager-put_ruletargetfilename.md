---
UID: NF:pla.IDataManager.put_RuleTargetFileName
title: IDataManager::put_RuleTargetFileName (pla.h)
description: Retrieves or sets the name of the report file that the TraceRpt.exe application creates. (IDataManager.put_RuleTargetFileName)
helpviewer_keywords: ["IDataManager interface [PLA]","RuleTargetFileName property","IDataManager.RuleTargetFileName","IDataManager.put_RuleTargetFileName","IDataManager::RuleTargetFileName","IDataManager::get_RuleTargetFileName","IDataManager::put_RuleTargetFileName","RuleTargetFileName property [PLA]","RuleTargetFileName property [PLA]","IDataManager interface","pla.idatamanager_ruletargetfilename","pla/IDataManager::RuleTargetFileName","pla/IDataManager::get_RuleTargetFileName","pla/IDataManager::put_RuleTargetFileName","put_RuleTargetFileName"]
old-location: pla\idatamanager_ruletargetfilename.htm
tech.root: PLA
ms.assetid: fc1484ea-c1d5-4267-bdf5-366c080bfc61
ms.date: 12/05/2018
ms.keywords: IDataManager interface [PLA],RuleTargetFileName property, IDataManager.RuleTargetFileName, IDataManager.put_RuleTargetFileName, IDataManager::RuleTargetFileName, IDataManager::get_RuleTargetFileName, IDataManager::put_RuleTargetFileName, RuleTargetFileName property [PLA], RuleTargetFileName property [PLA],IDataManager interface, pla.idatamanager_ruletargetfilename, pla/IDataManager::RuleTargetFileName, pla/IDataManager::get_RuleTargetFileName, pla/IDataManager::put_RuleTargetFileName, put_RuleTargetFileName
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
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDataManager::put_RuleTargetFileName
 - pla/IDataManager::put_RuleTargetFileName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataManager.RuleTargetFileName
 - IDataManager.get_RuleTargetFileName
 - IDataManager.put_RuleTargetFileName
---

# IDataManager::put_RuleTargetFileName


## -description

Retrieves or sets the name of the report file that the TraceRpt.exe application creates. 

This property is read/write.

## -parameters

## -remarks

PLA uses the file name only if you include the <b>plaCreateReport</b> value of the <a href="/windows/win32/api/pla/ne-pla-datamanagersteps">DataManagerSteps</a> enumeration in the <i>Steps</i> parameter of the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-run">IDataManager::Run</a> method.

To specify the contents of the report, use the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_reportschema">IDataManager::ReportSchema</a> property. To modify the contents of the report after it has been created, use the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_rules">IDataManager::Rules</a> property.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatamanager">IDataManager</a>
