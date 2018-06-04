---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

