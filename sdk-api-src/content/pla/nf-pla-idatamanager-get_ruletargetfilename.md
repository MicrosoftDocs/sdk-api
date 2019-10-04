---
UID: NF:pla.IDataManager.get_RuleTargetFileName
title: IDataManager::get_RuleTargetFileName (pla.h)
author: windows-sdk-content
description: Retrieves or sets the name of the report file that the TraceRpt.exe application creates.
old-location: pla\idatamanager_ruletargetfilename.htm
tech.root: PLA
ms.assetid: fc1484ea-c1d5-4267-bdf5-366c080bfc61
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDataManager interface [PLA],RuleTargetFileName property, IDataManager.RuleTargetFileName, IDataManager.get_RuleTargetFileName, IDataManager::RuleTargetFileName, IDataManager::get_RuleTargetFileName, IDataManager::put_RuleTargetFileName, RuleTargetFileName property [PLA], RuleTargetFileName property [PLA],IDataManager interface, get_RuleTargetFileName, pla.idatamanager_ruletargetfilename, pla/IDataManager::RuleTargetFileName, pla/IDataManager::get_RuleTargetFileName, pla/IDataManager::put_RuleTargetFileName
ms.topic: method
f1_keywords: 
 - "pla/IDataManager.RuleTargetFileName"
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
req.dll: Pla.dll
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataManager::get_RuleTargetFileName


## -description


Retrieves or sets the name of the report file that the TraceRpt.exe application creates. 

This property is read/write.


## -parameters


## -remarks



PLA uses the file name only if you include the <b>plaCreateReport</b> value of the <a href="https://docs.microsoft.com/windows/win32/api/pla/ne-pla-datamanagersteps">DataManagerSteps</a> enumeration in the <i>Steps</i> parameter of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-run">IDataManager::Run</a> method.

To specify the contents of the report, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_reportschema">IDataManager::ReportSchema</a> property. To modify the contents of the report after it has been created, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_rules">IDataManager::Rules</a> property.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-idatamanager">IDataManager</a>
 

 

