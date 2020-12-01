---
UID: NF:fsrmquota.IFsrmAutoApplyQuota.CommitAndUpdateDerived
title: IFsrmAutoApplyQuota::CommitAndUpdateDerived (fsrmquota.h)
description: Saves the quota and then applies any changes to the derived quotas.
helpviewer_keywords: ["CommitAndUpdateDerived","CommitAndUpdateDerived method [File Server Resource Manager]","CommitAndUpdateDerived method [File Server Resource Manager]","IFsrmAutoApplyQuota interface","IFsrmAutoApplyQuota interface [File Server Resource Manager]","CommitAndUpdateDerived method","IFsrmAutoApplyQuota.CommitAndUpdateDerived","IFsrmAutoApplyQuota::CommitAndUpdateDerived","fs.ifsrmautoapplyquota_commitandupdatederived","fsrm.ifsrmautoapplyquota_commitandupdatederived","fsrmquota/IFsrmAutoApplyQuota::CommitAndUpdateDerived"]
old-location: fsrm\ifsrmautoapplyquota_commitandupdatederived.htm
tech.root: fsrm
ms.assetid: f988b78d-214a-4f4f-81d4-d7f59fecb02a
ms.date: 12/05/2018
ms.keywords: CommitAndUpdateDerived, CommitAndUpdateDerived method [File Server Resource Manager], CommitAndUpdateDerived method [File Server Resource Manager],IFsrmAutoApplyQuota interface, IFsrmAutoApplyQuota interface [File Server Resource Manager],CommitAndUpdateDerived method, IFsrmAutoApplyQuota.CommitAndUpdateDerived, IFsrmAutoApplyQuota::CommitAndUpdateDerived, fs.ifsrmautoapplyquota_commitandupdatederived, fsrm.ifsrmautoapplyquota_commitandupdatederived, fsrmquota/IFsrmAutoApplyQuota::CommitAndUpdateDerived
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
 - IFsrmAutoApplyQuota::CommitAndUpdateDerived
 - fsrmquota/IFsrmAutoApplyQuota::CommitAndUpdateDerived
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
 - IFsrmAutoApplyQuota.CommitAndUpdateDerived
---

# IFsrmAutoApplyQuota::CommitAndUpdateDerived


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmautoquota">MSFT_FSRMAutoQuota</a> class.]

Saves the quota and then applies any changes to the derived quotas.

## -parameters

### -param commitOptions [in]

The options for saving the quota. For possible values, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmcommitoptions">FsrmCommitOptions</a> enumeration.

### -param applyOptions [in]

The options used to choose the derived quotas to which the changes are applied. For possible values, see 
      the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmtemplateapplyoptions">FsrmTemplateApplyOptions</a> enumeration.

### -param derivedObjectsResult [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmderivedobjectsresult">IFsrmDerivedObjectsResult</a> interface 
      that you use to determine the list of derived objects that were updated and whether the update was 
      successful.

## -returns

The method returns the following return values.

## -remarks

In this context, a derived quota is any quota that is  applied to  a subdirectory of the automatic quota 
    directory. For example, if you create an automatic quota for <i>c:\folder1</i> and if 
    <i>folder1</i> has subdirectories of <i>c:\folder1\subfolder1</i>, 
    <i>c:\folder1\subfolder2</i>, and <i>c:\folder1\subfolder3</i>, then a 
    quota that exists on <i>subfolder1</i>, <i>subfolder2</i>, or 
    <i>subfolder3</i> is considered a derived quota.

You would call this method if you called the 
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotaobject-applytemplate">ApplyTemplate</a> method to change the source 
    template for the automatic quota. Calling the 
    <b>CommitAndUpdateDerived</b> method 
    would then propagate the new template's settings to the existing quotas under the automatic quota directory.

If you specify the <b>FsrmTemplateApplyOptions_ApplyToDerivedAll</b> option, FSRM will 
    create a quota for all immediate subdirectories that do not have a quota applied to them and will update any 
    existing quotas using the properties of the automatic quota, whether the quota was created from the automatic 
    quota or not. For example, if a quota in one of the subdirectories was originally derived from a template, the 
    quota is considered a derived quota and is updated using the automatic quota—the quota is no 
    longer considered derived from the template.


#### Examples

For an example, see <a href="/previous-versions/windows/desktop/fsrm/updating-a-quota">Updating a Quota</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmautoapplyquota">IFsrmAutoApplyQuota</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmautoquota">MSFT_FSRMAutoQuota</a>