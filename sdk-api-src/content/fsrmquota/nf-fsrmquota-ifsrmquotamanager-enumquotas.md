---
UID: NF:fsrmquota.IFsrmQuotaManager.EnumQuotas
title: IFsrmQuotaManager::EnumQuotas (fsrmquota.h)
description: Enumerates the quotas for the specified directory and any quotas associated with its subdirectories (recursively).
helpviewer_keywords: ["EnumQuotas","EnumQuotas method [File Server Resource Manager]","EnumQuotas method [File Server Resource Manager]","FsrmQuotaManager class","EnumQuotas method [File Server Resource Manager]","IFsrmQuotaManager interface","EnumQuotas method [File Server Resource Manager]","IFsrmQuotaManagerEx interface","FsrmQuotaManager class [File Server Resource Manager]","EnumQuotas method","IFsrmQuotaManager interface [File Server Resource Manager]","EnumQuotas method","IFsrmQuotaManager.EnumQuotas","IFsrmQuotaManager::EnumQuotas","IFsrmQuotaManagerEx interface [File Server Resource Manager]","EnumQuotas method","IFsrmQuotaManagerEx::EnumQuotas","fs.ifsrmquotamanager_enumquotas","fsrm.ifsrmquotamanager_enumquotas","fsrmquota/IFsrmQuotaManager::EnumQuotas","fsrmquota/IFsrmQuotaManagerEx::EnumQuotas"]
old-location: fsrm\ifsrmquotamanager_enumquotas.htm
tech.root: fsrm
ms.assetid: 9977a519-4a6d-4b35-b973-4ef086e13e92
ms.date: 12/05/2018
ms.keywords: EnumQuotas, EnumQuotas method [File Server Resource Manager], EnumQuotas method [File Server Resource Manager],FsrmQuotaManager class, EnumQuotas method [File Server Resource Manager],IFsrmQuotaManager interface, EnumQuotas method [File Server Resource Manager],IFsrmQuotaManagerEx interface, FsrmQuotaManager class [File Server Resource Manager],EnumQuotas method, IFsrmQuotaManager interface [File Server Resource Manager],EnumQuotas method, IFsrmQuotaManager.EnumQuotas, IFsrmQuotaManager::EnumQuotas, IFsrmQuotaManagerEx interface [File Server Resource Manager],EnumQuotas method, IFsrmQuotaManagerEx::EnumQuotas, fs.ifsrmquotamanager_enumquotas, fsrm.ifsrmquotamanager_enumquotas, fsrmquota/IFsrmQuotaManager::EnumQuotas, fsrmquota/IFsrmQuotaManagerEx::EnumQuotas
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
 - IFsrmQuotaManager::EnumQuotas
 - fsrmquota/IFsrmQuotaManager::EnumQuotas
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
 - IFsrmQuotaManager.EnumQuotas
 - IFsrmQuotaManagerEx.EnumQuotas
 - FsrmQuotaManager.EnumQuotas
---

# IFsrmQuotaManager::EnumQuotas


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Enumerates the quotas for the specified directory and any quotas associated with its subdirectories 
    (recursively).

## -parameters

### -param path [in]

The local directory path that is associated with the quota that you want to enumerate. The string is limited 
       to 260 characters.

If the path ends with "\*", retrieve all quotas associated with the immediate subdirectories 
       of the path (does not include the quota associated with the path).

If the path ends with "\...", retrieve the quota for the path and all quotas associated with 
       the immediate subdirectories of the path (recursively).

If the path does not end in "\*" or "\...", retrieve the quota for the path 
       only.

If path is null or empty, the method returns all quotas.

### -param options [in]

Options to use when enumerating the quotas. For possible values, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmenumoptions">FsrmEnumOptions</a> enumeration.

### -param quotas [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcommittablecollection">IFsrmCommittableCollection</a> interface 
       that contains a collection of the quotas.

Each item of the collection is a <b>VARIANT</b> of type 
       <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for 
       the <a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquota">IFsrmQuota</a> interface.

The collection is empty if the path does not contain quotas.

## -returns

The method returns the following return values.

## -remarks

To enumerate quotas that apply automatically to the path's subdirectories, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumautoapplyquotas">IFsrmQuotaManager::EnumAutoApplyQuotas</a> 
    method.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmquotamanager">FsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanager">IFsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanagerex">IFsrmQuotaManagerEx</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>