---
UID: NF:fsrmquota.IFsrmQuotaTemplate.CommitAndUpdateDerived
title: IFsrmQuotaTemplate::CommitAndUpdateDerived (fsrmquota.h)
description: Saves the quota template and then applies any changes to the derived quota objects.
helpviewer_keywords: ["CommitAndUpdateDerived","CommitAndUpdateDerived method [File Server Resource Manager]","CommitAndUpdateDerived method [File Server Resource Manager]","IFsrmQuotaTemplate interface","IFsrmQuotaTemplate interface [File Server Resource Manager]","CommitAndUpdateDerived method","IFsrmQuotaTemplate.CommitAndUpdateDerived","IFsrmQuotaTemplate::CommitAndUpdateDerived","fs.ifsrmquotatemplate_commitandupdatederived","fsrm.ifsrmquotatemplate_commitandupdatederived","fsrmquota/IFsrmQuotaTemplate::CommitAndUpdateDerived"]
old-location: fsrm\ifsrmquotatemplate_commitandupdatederived.htm
tech.root: fsrm
ms.assetid: fecb034f-3f11-4d37-9468-56d4ea6268e7
ms.date: 12/05/2018
ms.keywords: CommitAndUpdateDerived, CommitAndUpdateDerived method [File Server Resource Manager], CommitAndUpdateDerived method [File Server Resource Manager],IFsrmQuotaTemplate interface, IFsrmQuotaTemplate interface [File Server Resource Manager],CommitAndUpdateDerived method, IFsrmQuotaTemplate.CommitAndUpdateDerived, IFsrmQuotaTemplate::CommitAndUpdateDerived, fs.ifsrmquotatemplate_commitandupdatederived, fsrm.ifsrmquotatemplate_commitandupdatederived, fsrmquota/IFsrmQuotaTemplate::CommitAndUpdateDerived
req.header: fsrmquota.h
req.include-header: 
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
 - IFsrmQuotaTemplate::CommitAndUpdateDerived
 - fsrmquota/IFsrmQuotaTemplate::CommitAndUpdateDerived
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
 - IFsrmQuotaTemplate.CommitAndUpdateDerived
---

# IFsrmQuotaTemplate::CommitAndUpdateDerived


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Saves the quota template and then applies any changes to the derived quota objects.

## -parameters

### -param commitOptions [in]

The options for saving the template. For possible values, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmcommitoptions">FsrmCommitOptions</a> enumeration.

### -param applyOptions [in]

The options used to choose the derived objects to which the changes are applied. For possible values, see 
      the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmtemplateapplyoptions">FsrmTemplateApplyOptions</a> enumeration.

### -param derivedObjectsResult [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmderivedobjectsresult">IFsrmDerivedObjectsResult</a> interface 
      that you use to determine the list of derived objects that were updated and whether the update was 
      successful.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotatemplate">IFsrmQuotaTemplate</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>