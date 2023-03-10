---
UID: NF:fsrmquota.IFsrmQuotaManager.EnumAutoApplyQuotas
title: IFsrmQuotaManager::EnumAutoApplyQuotas (fsrmquota.h)
description: Enumerates the automatic quotas that are associated with the specified directory.
helpviewer_keywords: ["EnumAutoApplyQuotas","EnumAutoApplyQuotas method [File Server Resource Manager]","EnumAutoApplyQuotas method [File Server Resource Manager]","FsrmQuotaManager class","EnumAutoApplyQuotas method [File Server Resource Manager]","IFsrmQuotaManager interface","EnumAutoApplyQuotas method [File Server Resource Manager]","IFsrmQuotaManagerEx interface","FsrmQuotaManager class [File Server Resource Manager]","EnumAutoApplyQuotas method","IFsrmQuotaManager interface [File Server Resource Manager]","EnumAutoApplyQuotas method","IFsrmQuotaManager.EnumAutoApplyQuotas","IFsrmQuotaManager::EnumAutoApplyQuotas","IFsrmQuotaManagerEx interface [File Server Resource Manager]","EnumAutoApplyQuotas method","IFsrmQuotaManagerEx::EnumAutoApplyQuotas","fs.ifsrmquotamanager_enumautoapplyquotas","fsrm.ifsrmquotamanager_enumautoapplyquotas","fsrmquota/IFsrmQuotaManager::EnumAutoApplyQuotas","fsrmquota/IFsrmQuotaManagerEx::EnumAutoApplyQuotas"]
old-location: fsrm\ifsrmquotamanager_enumautoapplyquotas.htm
tech.root: fsrm
ms.assetid: 6542bc4e-535f-4e6c-aaa8-ba6963490811
ms.date: 12/05/2018
ms.keywords: EnumAutoApplyQuotas, EnumAutoApplyQuotas method [File Server Resource Manager], EnumAutoApplyQuotas method [File Server Resource Manager],FsrmQuotaManager class, EnumAutoApplyQuotas method [File Server Resource Manager],IFsrmQuotaManager interface, EnumAutoApplyQuotas method [File Server Resource Manager],IFsrmQuotaManagerEx interface, FsrmQuotaManager class [File Server Resource Manager],EnumAutoApplyQuotas method, IFsrmQuotaManager interface [File Server Resource Manager],EnumAutoApplyQuotas method, IFsrmQuotaManager.EnumAutoApplyQuotas, IFsrmQuotaManager::EnumAutoApplyQuotas, IFsrmQuotaManagerEx interface [File Server Resource Manager],EnumAutoApplyQuotas method, IFsrmQuotaManagerEx::EnumAutoApplyQuotas, fs.ifsrmquotamanager_enumautoapplyquotas, fsrm.ifsrmquotamanager_enumautoapplyquotas, fsrmquota/IFsrmQuotaManager::EnumAutoApplyQuotas, fsrmquota/IFsrmQuotaManagerEx::EnumAutoApplyQuotas
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
 - IFsrmQuotaManager::EnumAutoApplyQuotas
 - fsrmquota/IFsrmQuotaManager::EnumAutoApplyQuotas
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
 - IFsrmQuotaManager.EnumAutoApplyQuotas
 - IFsrmQuotaManagerEx.EnumAutoApplyQuotas
 - FsrmQuotaManager.EnumAutoApplyQuotas
---

# IFsrmQuotaManager::EnumAutoApplyQuotas


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Enumerates the automatic quotas that are associated with the specified directory. The 
    enumeration can also include automatic quotas associated with  subdirectories (recursively).

## -parameters

### -param path [in]

The local directory path that is associated with the automatic quota that you want to enumerate. The string 
       is limited to 260 characters.

If the path ends with "\*", retrieve all automatic quotas associated with the immediate 
       subdirectories of the path (does not include the quota associated with the path).

If the path ends with "\...", retrieve the automatic quota for the path and all automatic 
       quotas associated with the immediate subdirectories of the path (recursively).

If the path does not end in "\*" or "\...", retrieve the automatic quota 
       for the path only.

If path is null or empty, the method returns all quotas.

### -param options [in]

Options to use when enumerating the quotas. For possible values, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmenumoptions">FsrmEnumOptions</a> enumeration.

### -param quotas [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcommittablecollection">IFsrmCommittableCollection</a> interface 
       that contains a collection of the automatic quotas.

Each item of the collection is a <b>VARIANT</b> of type 
       <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for 
       the <a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmautoapplyquota">IFsrmAutoApplyQuota</a> interface.

The collection is empty if the path does not contain quotas.

## -returns

The method returns the following return values.

## -remarks

To enumerate quotas that do not automatically apply to the path's subdirectories, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumquotas">IFsrmQuotaManager::EnumQuotas</a> 
    method.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmquotamanager">FsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanager">IFsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanagerex">IFsrmQuotaManagerEx</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>