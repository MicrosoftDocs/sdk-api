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

# IFsrmSetting::get_SmtpServer


## -description


Retrieves or sets the SMTP server that FSRM uses to send email.

This property is read/write.


## -parameters


## -remarks



This property must be set in order for FSRM to send email. To verify settings, call the 
    <a href="https://msdn.microsoft.com/dda57309-8e77-4934-bb3e-d208d4607ea5">IFsrmSetting::EmailTest</a> method.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/dda57309-8e77-4934-bb3e-d208d4607ea5">IFsrmSetting::EmailTest</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0c27393a-9a84-4147-a7e0-582c0bf2d918">FsrmSetting</a>



<a href="https://msdn.microsoft.com/432fbaaa-7ddb-4d8c-bfbe-40cd26b08f9b">IFsrmSetting</a>
 

 

