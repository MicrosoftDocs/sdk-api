---
UID: NN:fsrm.IFsrmCommittableCollection
title: IFsrmCommittableCollection
author: windows-sdk-content
description: Defines a collection of FSRM objects that can have the same type of objects added to or removed from the collection. All objects in the collection can also be committed in a single batch operation.
old-location: fsrm\ifsrmcommittablecollection.htm
old-project: Fsrm
ms.assetid: ef4678b4-e6b0-4044-ba11-7a3ae01ad2c7
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: IFsrmCommittableCollection, IFsrmCommittableCollection interface [File Server Resource Manager], IFsrmCommittableCollection interface [File Server Resource Manager],described, fs.ifsrmcommitablecollection, fs.ifsrmcommittablecollection, fsrm.ifsrmcommittablecollection, fsrm/IFsrmCommittableCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FILTERED_DATA_SOURCES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmCommittableCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmCommittableCollection interface


## -description


Defines a collection of FSRM objects that can have the same type of objects added to or removed from 
    the collection. All objects in the collection can also be committed in a single batch operation. 
    Committing objects in a batch operation provides better performance than committing each object in the collection 
    individually.

To create an empty collection, call the 
    <a href="https://msdn.microsoft.com/88656cb9-1e72-4f82-ac09-fbb3c8a36afc">IFsrmQuotaManager::CreateQuotaCollection</a> 
    method.

The following methods and properties return this collection:
<ul>
<li>
<a href="https://msdn.microsoft.com/d8d18971-ba3e-4e20-83ff-1290bc453b90">IFsrmExportImport::ImportFileGroups</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ea2fbd88-777e-454c-8d32-0d704c219558">IFsrmExportImport::ImportFileScreenTemplates</a>
</li>
<li>
<a href="https://msdn.microsoft.com/90b70f64-fbc7-48d2-9cf7-71e625ed32af">IFsrmExportImport::ImportQuotaTemplates</a>
</li>
<li>
<a href="https://msdn.microsoft.com/317eb6cf-7bcc-4042-a7b7-05efac84a0c2">IFsrmFileGroupManager::EnumFileGroups</a>
</li>
<li>
<a href="https://msdn.microsoft.com/81f62d49-5fce-4d8c-96b5-506d741c5f77">IFsrmFileGroupManager::ImportFileGroups</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4adce5d6-8be6-477b-8dab-d437163b4449">IFsrmFileScreenManager::CreateFileScreenCollection</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5826d5c3-885a-4001-aa89-0bc1c03b9338">IFsrmFileScreenManager::EnumFileScreens</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c30377c8-d3a3-40fe-a42c-9b36d2a0b35e">IFsrmFileScreenManager::EnumFileScreenExceptions</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5bfb82f9-50a5-4266-956d-f99e2982a6a5">IFsrmFileScreenTemplateManager::EnumTemplates</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0660a1cb-904e-4ed0-bbc8-9903e8848f4e">IFsrmFileScreenTemplateManager::ImportTemplates</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6542bc4e-535f-4e6c-aaa8-ba6963490811">IFsrmQuotaManager::EnumAutoApplyQuotas</a>
</li>
<li>
<a href="https://msdn.microsoft.com/abe5e73b-459a-4e2a-9917-91d3c85a15bc">IFsrmQuotaManager::EnumEffectiveQuotas</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9977a519-4a6d-4b35-b973-4ef086e13e92">IFsrmQuotaManager::EnumQuotas</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e5f5b94a-6b17-4379-9141-07ec70a830e9">IFsrmQuotaTemplateManager::EnumTemplates</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f530d7fc-8b41-4a5e-a10a-b9211c7fe2bb">IFsrmQuotaTemplateManager::ImportTemplates</a>
</li>
</ul>The collection is empty if the 
    <a href="https://msdn.microsoft.com/47ea1193-0afe-4036-b8b5-511fa2e013be">IFsrmCollection::Count</a> property is zero.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmCommittableCollection</b> interface inherits from <a href="https://msdn.microsoft.com/e41f01ef-5dd2-4066-82cd-45b57578c9bb">IFsrmMutableCollection</a>. <b>IFsrmCommittableCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsrmCommittableCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a>
</td>
<td align="left" width="63%">
Commits all the objects of the collection and returns the commit results for each object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e41f01ef-5dd2-4066-82cd-45b57578c9bb">IFsrmMutableCollection</a>
 

 

