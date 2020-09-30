---
UID: NF:fsrmquota.IFsrmQuotaManager.EnumEffectiveQuotas
title: IFsrmQuotaManager::EnumEffectiveQuotas (fsrmquota.h)
description: Enumerates all the quotas that affect the specified path.
helpviewer_keywords: ["EnumEffectiveQuotas","EnumEffectiveQuotas method [File Server Resource Manager]","EnumEffectiveQuotas method [File Server Resource Manager]","FsrmQuotaManager class","EnumEffectiveQuotas method [File Server Resource Manager]","IFsrmQuotaManager interface","EnumEffectiveQuotas method [File Server Resource Manager]","IFsrmQuotaManagerEx interface","FsrmQuotaManager class [File Server Resource Manager]","EnumEffectiveQuotas method","IFsrmQuotaManager interface [File Server Resource Manager]","EnumEffectiveQuotas method","IFsrmQuotaManager.EnumEffectiveQuotas","IFsrmQuotaManager::EnumEffectiveQuotas","IFsrmQuotaManagerEx interface [File Server Resource Manager]","EnumEffectiveQuotas method","IFsrmQuotaManagerEx::EnumEffectiveQuotas","fs.ifsrmquotamanager_enumeffectivequotas","fsrm.ifsrmquotamanager_enumeffectivequotas","fsrmquota/IFsrmQuotaManager::EnumEffectiveQuotas","fsrmquota/IFsrmQuotaManagerEx::EnumEffectiveQuotas"]
old-location: fsrm\ifsrmquotamanager_enumeffectivequotas.htm
tech.root: fsrm
ms.assetid: abe5e73b-459a-4e2a-9917-91d3c85a15bc
ms.date: 12/05/2018
ms.keywords: EnumEffectiveQuotas, EnumEffectiveQuotas method [File Server Resource Manager], EnumEffectiveQuotas method [File Server Resource Manager],FsrmQuotaManager class, EnumEffectiveQuotas method [File Server Resource Manager],IFsrmQuotaManager interface, EnumEffectiveQuotas method [File Server Resource Manager],IFsrmQuotaManagerEx interface, FsrmQuotaManager class [File Server Resource Manager],EnumEffectiveQuotas method, IFsrmQuotaManager interface [File Server Resource Manager],EnumEffectiveQuotas method, IFsrmQuotaManager.EnumEffectiveQuotas, IFsrmQuotaManager::EnumEffectiveQuotas, IFsrmQuotaManagerEx interface [File Server Resource Manager],EnumEffectiveQuotas method, IFsrmQuotaManagerEx::EnumEffectiveQuotas, fs.ifsrmquotamanager_enumeffectivequotas, fsrm.ifsrmquotamanager_enumeffectivequotas, fsrmquota/IFsrmQuotaManager::EnumEffectiveQuotas, fsrmquota/IFsrmQuotaManagerEx::EnumEffectiveQuotas
req.header: fsrmquota.h
req.include-header: FsrmQuota.h, FsrmTlb.h
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
 - IFsrmQuotaManager::EnumEffectiveQuotas
 - fsrmquota/IFsrmQuotaManager::EnumEffectiveQuotas
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
 - IFsrmQuotaManager.EnumEffectiveQuotas
 - IFsrmQuotaManagerEx.EnumEffectiveQuotas
 - FsrmQuotaManager.EnumEffectiveQuotas
---

# IFsrmQuotaManager::EnumEffectiveQuotas


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Enumerates all the quotas that affect the specified path.

## -parameters

### -param path [in]

A local directory path. The string is limited to 260 characters.

### -param options [in]

Options to use when enumerating the quotas. For possible values, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmenumoptions">FsrmEnumOptions</a> enumeration.

### -param quotas [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcommittablecollection">IFsrmCommittableCollection</a> interface 
       that contains a collection of the quotas configured at or above the specified path.

Each item of the collection is a <b>VARIANT</b> of type 
       <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for 
       the <a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquota">IFsrmQuota</a> interface.

The collection is empty if the path does not contain quotas.

## -returns

The method returns the following return values.

## -remarks

Does not enumerate automatic quotas. To enumerate automatic quotas, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumautoapplyquotas">IFsrmQuotaManager::EnumAutoApplyQuotas</a> 
    method.

To enumerate all quotas, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumquotas">IFsrmQuotaManager::EnumQuotas</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmquotamanager">FsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanager">IFsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanagerex">IFsrmQuotaManagerEx</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>