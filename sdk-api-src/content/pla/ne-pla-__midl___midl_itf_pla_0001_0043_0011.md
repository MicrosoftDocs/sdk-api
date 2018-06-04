---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __MIDL___MIDL_itf_pla_0001_0043_0011 enumeration


## -description


Defines the actions that the data manager takes when it runs.


## -enum-fields




### -field plaCreateReport

Runs TraceRpt.exe using as input all the binary performance files (.blg) or event trace files (.etl) in the collection. You can use the <a href="https://msdn.microsoft.com/32620e9d-9541-4c39-9312-937b0b4825ad">IDataManager::ReportSchema</a> property to customize the report.

The <a href="https://msdn.microsoft.com/fc1484ea-c1d5-4267-bdf5-366c080bfc61">IDataManager::RuleTargetFileName</a> property contains the name of the file that TraceRpt creates.


### -field plaRunRules

If a report exists, apply the rules specified in the <a href="https://msdn.microsoft.com/17403e57-2eea-4a2b-a75c-66f486622078">IDataManager::Rules</a> property to the report.

The <a href="https://msdn.microsoft.com/fc1484ea-c1d5-4267-bdf5-366c080bfc61">RuleTargetFileName</a> property contains the name of the file to which the rules are applied.


### -field plaCreateHtml

Converts the XML file specified in <a href="https://msdn.microsoft.com/fc1484ea-c1d5-4267-bdf5-366c080bfc61">RuleTargetFileName</a> to HTML format. The HTML format is written to the file specified in the <a href="https://msdn.microsoft.com/5b4c1d99-2f41-423a-b019-845dcd61d516">IDataManager::ReportFileName</a> property.


### -field plaFolderActions

Apply the folder actions specified in the <a href="https://msdn.microsoft.com/59fad3d2-9971-4608-8576-977d4dd8ace4">IDataManager::FolderActions</a> property to all folders defined in the collection.


### -field plaResourceFreeing

If the <a href="https://msdn.microsoft.com/71368635-e8c3-44fd-9d8a-f225b10225ba">IDataManager::MaxFolderCount</a>, <a href="https://msdn.microsoft.com/a9508617-acb5-4e11-8f4a-72c8e5cb4cba">IDataManager::MaxSize</a>, or <a href="https://msdn.microsoft.com/e5f4f752-ae96-4a1b-99a4-ff3b73fe3743">IDataManager::MinFreeDisk</a> property exceeds its limit, apply the resource policy specified in the <a href="https://msdn.microsoft.com/541cd28c-2e01-4b8a-9cd3-044896c8fb80">IDataManager::ResourcePolicy</a> property.


## -remarks



Specify one or more actions. The data manager applies the actions in the order in which they are defined in this enumeration.




## -see-also




<a href="https://msdn.microsoft.com/a1016784-8841-485f-885e-3719bdb0ae05">IDataManager::Run</a>
 

 

