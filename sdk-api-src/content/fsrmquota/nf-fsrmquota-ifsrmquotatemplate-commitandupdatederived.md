---
UID: NF:fsrmquota.IFsrmQuotaTemplate.CommitAndUpdateDerived
title: IFsrmQuotaTemplate::CommitAndUpdateDerived (fsrmquota.h)
author: windows-sdk-content
description: Saves the quota template and then applies any changes to the derived quota objects.
old-location: fsrm\ifsrmquotatemplate_commitandupdatederived.htm
tech.root: fsrm
ms.assetid: fecb034f-3f11-4d37-9468-56d4ea6268e7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CommitAndUpdateDerived, CommitAndUpdateDerived method [File Server Resource Manager], CommitAndUpdateDerived method [File Server Resource Manager],IFsrmQuotaTemplate interface, IFsrmQuotaTemplate interface [File Server Resource Manager],CommitAndUpdateDerived method, IFsrmQuotaTemplate.CommitAndUpdateDerived, IFsrmQuotaTemplate::CommitAndUpdateDerived, fs.ifsrmquotatemplate_commitandupdatederived, fsrm.ifsrmquotatemplate_commitandupdatederived, fsrmquota/IFsrmQuotaTemplate::CommitAndUpdateDerived
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmQuotaTemplate.CommitAndUpdateDerived
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmQuotaTemplate::CommitAndUpdateDerived


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Saves the quota template and then applies any changes to the derived quota objects.


## -parameters




### -param commitOptions [in]

The options for saving the template. For possible values, see the 
      <a href="https://msdn.microsoft.com/eb362bd8-c11f-404e-be54-0e16007494a7">FsrmCommitOptions</a> enumeration.


### -param applyOptions [in]

The options used to choose the derived objects to which the changes are applied. For possible values, see 
      the <a href="https://msdn.microsoft.com/44a8e280-4005-476c-a43d-184c18825129">FsrmTemplateApplyOptions</a> enumeration.


### -param derivedObjectsResult [out]

An <a href="https://msdn.microsoft.com/1486d53a-d09a-4eff-ba07-b9dbb32e18ba">IFsrmDerivedObjectsResult</a> interface 
      that you use to determine the list of derived objects that were updated and whether the update was 
      successful.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/de8ac383-f309-4320-bc77-c859ba27e1ca">IFsrmQuotaTemplate</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

