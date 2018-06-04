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

# IFsrmClassificationManager::put_Logging


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

The types of logging to perform when running the classification rules.

This property is read/write.


## -parameters


## -remarks



The log file for the <b>FsrmClassificationLoggingFlags_ClassificationsInLogFile</b> and 
    <b>FsrmClassificationLoggingFlags_ErrorsInLogFile</b> logging options are stored in the 
    reports directory. The name of the 
    <b>FsrmClassificationLoggingFlags_ClassificationsInLogFile</b> log file is 
    "<i>ClassifierName</i>-<i>FsrmServerName(FQDN)</i>-<i>TimeStamp</i>.xml". 
    The log file contains one entry per property assignment to a specific file. Each log entry specifies the:

<ul>
<li>File name (full path)</li>
<li>Property</li>
<li>Value assigned</li>
<li>Rule applied</li>
<li>Result (whether the classification succeeded)</li>
</ul>
The name of the <b>FsrmClassificationLoggingFlags_ErrorsInLogFile</b> log file is 
    "<i>ClassifierName</i><i>Errors</i>-<i>FQDNServerName</i>-<i>TimeStamp</i>.xml". 
    The log file contains one entry per error. Each log entry specifies the:

<ul>
<li>Error code</li>
<li>File name (full path)</li>
<li>Property</li>
<li>Rule applied</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

