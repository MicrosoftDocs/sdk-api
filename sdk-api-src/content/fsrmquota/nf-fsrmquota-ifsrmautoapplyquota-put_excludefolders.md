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

# IFsrmAutoApplyQuota::put_ExcludeFolders


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/3941d07c-67e3-4763-8113-31fc156c9bd0">MSFT_FSRMAutoQuota</a> class.]

Retrieves or sets an array of immediate subdirectories to exclude from the automatic 
    quota.

This property is read/write.


## -parameters


## -remarks



The list can contain the names of existing subdirectories or subdirectories that may exist in the future.

Setting this property overwrites the current list of subdirectories to exclude. To remove all folders, pass an 
    empty array.




## -see-also




<a href="https://msdn.microsoft.com/3eb30caa-ce29-4898-b1a7-bd905031ca98">IFsrmAutoApplyQuota</a>



<a href="https://msdn.microsoft.com/3941d07c-67e3-4763-8113-31fc156c9bd0">MSFT_FSRMAutoQuota</a>
 

 

