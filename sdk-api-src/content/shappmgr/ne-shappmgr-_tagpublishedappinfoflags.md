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

# _tagPublishedAppInfoFlags enumeration


## -description


Specifies which members in the <a href="https://msdn.microsoft.com/927c58d3-4208-4fd3-a3fa-18ae7d8d3136">PUBAPPINFO</a> structure are valid. These flags are bitmasks set in the <b>dwMask</b> member and passed to <a href="https://msdn.microsoft.com/4ffcc30a-cf07-45e7-b9a5-342fe2b553c8">IPublishedApp::GetPublishedAppInfo</a>.


## -enum-fields




### -field PAI_SOURCE

The <a href="https://msdn.microsoft.com/927c58d3-4208-4fd3-a3fa-18ae7d8d3136">pszSource</a> string is valid and contains the display name of the publishing source. If multiple sources publish an application of the same name, Add/Remove Programs identifies them by "&lt;application name&gt; : &lt;publishing source&gt;".


### -field PAI_ASSIGNEDTIME

The <a href="https://msdn.microsoft.com/927c58d3-4208-4fd3-a3fa-18ae7d8d3136">stAssigned</a> member is valid and contains the time that the application should be installed as assigned by an application administrator.


### -field PAI_PUBLISHEDTIME

Not used.


### -field PAI_SCHEDULEDTIME

The <a href="https://msdn.microsoft.com/927c58d3-4208-4fd3-a3fa-18ae7d8d3136">stScheduled</a> member is valid and contains the time that the application should be installed as assigned by the user.


### -field PAI_EXPIRETIME

The <a href="https://msdn.microsoft.com/927c58d3-4208-4fd3-a3fa-18ae7d8d3136">stExpired</a> member is valid and contains the time after which Add/Remove Programs should no longer install the program.


## -see-also




<a href="https://msdn.microsoft.com/4ffcc30a-cf07-45e7-b9a5-342fe2b553c8">IPublishedApp::GetPublishedAppInfo</a>
 

 

