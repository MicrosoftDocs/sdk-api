---
UID: NF:fsrmscreen.IFsrmFileScreenTemplate.CommitAndUpdateDerived
title: IFsrmFileScreenTemplate::CommitAndUpdateDerived (fsrmscreen.h)
description: Saves the file screen template and then applies any changes to the derived file screen objects.
helpviewer_keywords: ["CommitAndUpdateDerived","CommitAndUpdateDerived method [File Server Resource Manager]","CommitAndUpdateDerived method [File Server Resource Manager]","IFsrmFileScreenTemplate interface","IFsrmFileScreenTemplate interface [File Server Resource Manager]","CommitAndUpdateDerived method","IFsrmFileScreenTemplate.CommitAndUpdateDerived","IFsrmFileScreenTemplate::CommitAndUpdateDerived","fs.ifsrmfilescreentemplate_commitandupdatederived","fsrm.ifsrmfilescreentemplate_commitandupdatederived","fsrmscreen/IFsrmFileScreenTemplate::CommitAndUpdateDerived"]
old-location: fsrm\ifsrmfilescreentemplate_commitandupdatederived.htm
tech.root: fsrm
ms.assetid: 6b50a93f-f6f0-4ab4-a4a3-3995b721c5d7
ms.date: 12/05/2018
ms.keywords: CommitAndUpdateDerived, CommitAndUpdateDerived method [File Server Resource Manager], CommitAndUpdateDerived method [File Server Resource Manager],IFsrmFileScreenTemplate interface, IFsrmFileScreenTemplate interface [File Server Resource Manager],CommitAndUpdateDerived method, IFsrmFileScreenTemplate.CommitAndUpdateDerived, IFsrmFileScreenTemplate::CommitAndUpdateDerived, fs.ifsrmfilescreentemplate_commitandupdatederived, fsrm.ifsrmfilescreentemplate_commitandupdatederived, fsrmscreen/IFsrmFileScreenTemplate::CommitAndUpdateDerived
req.header: fsrmscreen.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmScreen.idl
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
 - IFsrmFileScreenTemplate::CommitAndUpdateDerived
 - fsrmscreen/IFsrmFileScreenTemplate::CommitAndUpdateDerived
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
 - IFsrmFileScreenTemplate.CommitAndUpdateDerived
---

# IFsrmFileScreenTemplate::CommitAndUpdateDerived


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreentemplate">MSFT_FSRMFileScreenTemplate</a> class.]

Saves the file screen template and then applies any changes to the derived file screen 
    objects.

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

<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreentemplate">IFsrmFileScreenTemplate</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreentemplate">MSFT_FSRMFileScreenTemplate</a>