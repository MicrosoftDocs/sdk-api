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

# IFsrmFileScreenException interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1787aab2-b315-418c-81bf-1e42198c8780">MSFT_FSRMFileScreenException</a> class.]

Used to configure an exception that excludes the specified files from the file screening 
    process. This allows the  files of a file group to be saved in the directory when a file screen that 
    applies to the directory would otherwise prevent the file from being saved in the directory.

To create this interface, call the 
    <a href="https://msdn.microsoft.com/b2a15f69-49fb-46fd-9219-aa970c9eb042">IFsrmFileScreenManager::CreateFileScreenException</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/c30377c8-d3a3-40fe-a42c-9b36d2a0b35e">IFsrmFileScreenManager::EnumFileScreenExceptions</a>
</li>
<li>
<a href="https://msdn.microsoft.com/634c54b0-2766-4248-8a27-506eaa3d6a68">IFsrmFileScreenManager::GetFileScreenException</a>
</li>
</ul>

## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/bb08ea40-6f0e-4ad5-ad57-78f17bbbd4b7">IFsrmObject</a>



<a href="https://msdn.microsoft.com/1787aab2-b315-418c-81bf-1e42198c8780">MSFT_FSRMFileScreenException</a>
 

 

