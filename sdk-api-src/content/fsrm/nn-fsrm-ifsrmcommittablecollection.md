---
UID: NN:fsrm.IFsrmCommittableCollection
title: IFsrmCommittableCollection (fsrm.h)
description: Defines a collection of FSRM objects that can have the same type of objects added to or removed from the collection. All objects in the collection can also be committed in a single batch operation.
helpviewer_keywords: ["IFsrmCommittableCollection","IFsrmCommittableCollection interface [File Server Resource Manager]","IFsrmCommittableCollection interface [File Server Resource Manager]","described","fs.ifsrmcommitablecollection","fs.ifsrmcommittablecollection","fsrm.ifsrmcommittablecollection","fsrm/IFsrmCommittableCollection"]
old-location: fsrm\ifsrmcommittablecollection.htm
tech.root: fsrm
ms.assetid: ef4678b4-e6b0-4044-ba11-7a3ae01ad2c7
ms.date: 12/05/2018
ms.keywords: IFsrmCommittableCollection, IFsrmCommittableCollection interface [File Server Resource Manager], IFsrmCommittableCollection interface [File Server Resource Manager],described, fs.ifsrmcommitablecollection, fs.ifsrmcommittablecollection, fsrm.ifsrmcommittablecollection, fsrm/IFsrmCommittableCollection
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
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmCommittableCollection
 - fsrm/IFsrmCommittableCollection
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
 - IFsrmCommittableCollection
---

# IFsrmCommittableCollection interface


## -description

Defines a collection of FSRM objects that can have the same type of objects added to or removed from 
    the collection. All objects in the collection can also be committed in a single batch operation. 
    Committing objects in a batch operation provides better performance than committing each object in the collection 
    individually.

To create an empty collection, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-createquotacollection">IFsrmQuotaManager::CreateQuotaCollection</a> 
    method.

The following methods and properties return this collection:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmexportimport-importfilegroups">IFsrmExportImport::ImportFileGroups</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmexportimport-importfilescreentemplates">IFsrmExportImport::ImportFileScreenTemplates</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmexportimport-importquotatemplates">IFsrmExportImport::ImportQuotaTemplates</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-enumfilegroups">IFsrmFileGroupManager::EnumFileGroups</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-importfilegroups">IFsrmFileGroupManager::ImportFileGroups</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-createfilescreencollection">IFsrmFileScreenManager::CreateFileScreenCollection</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-enumfilescreens">IFsrmFileScreenManager::EnumFileScreens</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-enumfilescreenexceptions">IFsrmFileScreenManager::EnumFileScreenExceptions</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplatemanager-enumtemplates">IFsrmFileScreenTemplateManager::EnumTemplates</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplatemanager-importtemplates">IFsrmFileScreenTemplateManager::ImportTemplates</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumautoapplyquotas">IFsrmQuotaManager::EnumAutoApplyQuotas</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumeffectivequotas">IFsrmQuotaManager::EnumEffectiveQuotas</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumquotas">IFsrmQuotaManager::EnumQuotas</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplatemanager-enumtemplates">IFsrmQuotaTemplateManager::EnumTemplates</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplatemanager-importtemplates">IFsrmQuotaTemplateManager::ImportTemplates</a>
</li>
</ul>The collection is empty if the 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcollection-get_count">IFsrmCollection::Count</a> property is zero.

## -inheritance

The <b>IFsrmCommittableCollection</b> interface inherits from <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmmutablecollection">IFsrmMutableCollection</a>. <b>IFsrmCommittableCollection</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmmutablecollection">IFsrmMutableCollection</a>
