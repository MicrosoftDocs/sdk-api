---
UID: NF:pla.IDataManager.get_RuleTargetFileName
title: IDataManager::get_RuleTargetFileName method
author: windows-driver-content
description: Retrieves or sets the name of the report file that the TraceRpt.exe application creates.
old-location: pla\idatamanager_ruletargetfilename.htm
old-project: PLA
ms.assetid: fc1484ea-c1d5-4267-bdf5-366c080bfc61
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IDataManager, IDataManager interface [PLA], RuleTargetFileName property, IDataManager.RuleTargetFileName, IDataManager::get_RuleTargetFileName, IDataManager::put_RuleTargetFileName, RuleTargetFileName property [PLA], RuleTargetFileName property [PLA], IDataManager interface, get_RuleTargetFileName,IDataManager.get_RuleTargetFileName, pla.idatamanager_ruletargetfilename, pla/IDataManager::RuleTargetFileName, pla/IDataManager::get_RuleTargetFileName, pla/IDataManager::put_RuleTargetFileName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	IDataManager.RuleTargetFileName
-	IDataManager.get_RuleTargetFileName
-	IDataManager.put_RuleTargetFileName
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IDataManager::get_RuleTargetFileName method


## -description


Retrieves or sets the name of the report file that the TraceRpt.exe application creates. 

This property is read/write.


## -parameters


## -remarks



PLA uses the file name only if you include the <b>plaCreateReport</b> value of the <a href="https://msdn.microsoft.com/e647987d-e524-475e-a355-539cb3f04635">DataManagerSteps</a> enumeration in the <i>Steps</i> parameter of the <a href="https://msdn.microsoft.com/a1016784-8841-485f-885e-3719bdb0ae05">IDataManager::Run</a> method.

To specify the contents of the report, use the <a href="https://msdn.microsoft.com/32620e9d-9541-4c39-9312-937b0b4825ad">IDataManager::ReportSchema</a> property. To modify the contents of the report after it has been created, use the <a href="https://msdn.microsoft.com/17403e57-2eea-4a2b-a75c-66f486622078">IDataManager::Rules</a> property.




## -see-also




<a href="https://msdn.microsoft.com/a153d88f-4c7e-45fd-9cd8-497160711de4">IDataManager</a>
 

 

