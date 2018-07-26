---
UID: NF:fsrmscreen.IFsrmFileScreenTemplate.CommitAndUpdateDerived
title: IFsrmFileScreenTemplate::CommitAndUpdateDerived
author: windows-sdk-content
description: Saves the file screen template and then applies any changes to the derived file screen objects.
old-location: fsrm\ifsrmfilescreentemplate_commitandupdatederived.htm
old-project: Fsrm
ms.assetid: 6b50a93f-f6f0-4ab4-a4a3-3995b721c5d7
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: CommitAndUpdateDerived, CommitAndUpdateDerived method [File Server Resource Manager], CommitAndUpdateDerived method [File Server Resource Manager],IFsrmFileScreenTemplate interface, IFsrmFileScreenTemplate interface [File Server Resource Manager],CommitAndUpdateDerived method, IFsrmFileScreenTemplate.CommitAndUpdateDerived, IFsrmFileScreenTemplate::CommitAndUpdateDerived, fs.ifsrmfilescreentemplate_commitandupdatederived, fsrm.ifsrmfilescreentemplate_commitandupdatederived, fsrmscreen/IFsrmFileScreenTemplate::CommitAndUpdateDerived
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmFileScreenTemplate.CommitAndUpdateDerived
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileScreenTemplate::CommitAndUpdateDerived


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/be4f3a6a-280f-4b0f-afdf-ce1ee7933018">MSFT_FSRMFileScreenTemplate</a> class.]

Saves the file screen template and then applies any changes to the derived file screen 
    objects.


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




<a href="https://msdn.microsoft.com/c8e612f5-e7cd-45ff-9eaf-9d1674231161">IFsrmFileScreenTemplate</a>



<a href="https://msdn.microsoft.com/be4f3a6a-280f-4b0f-afdf-ce1ee7933018">MSFT_FSRMFileScreenTemplate</a>
 

 

