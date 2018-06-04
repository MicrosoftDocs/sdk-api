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

# IAutomaticUpdatesSettings::get_ReadOnly


## -description


<p class="CCE_Message">[<b>IAutomaticUpdatesSettings::ReadOnly</b> is no longer supported. Starting with 
    Windows 10 calls to <b>ReadOnly</b> always return <b>VARIANT_FALSE</b>. However, <b>IAutomaticUpdatesSettings::Save</b> is a no-op, so no changes can be made.]


Gets a Boolean value that indicates whether the Automatic Update settings are read-only.



This property is read-only.


## -parameters


## -remarks



<b>ReadOnly</b> is <b>VARIANT_TRUE</b> if either of the following conditions is true:

<ul>
<li>The caller has insufficient security permissions to modify the Automatic Updates settings.</li>
<li>The current settings are enforced by Group Policy.
</li>
</ul>
 
The caller can modify the settings in the  <a href="https://msdn.microsoft.com/c4672df5-9e47-45f5-9504-1ebb0bf3c6a6">IAutomaticUpdatesSettings</a> interface only if <b>ReadOnly</b> is <b>VARIANT_FALSE</b>.
The value of <b>ReadOnly</b> may change after calling <a href="https://msdn.microsoft.com/308426d9-d524-406a-931c-1fdb854aa4fb">Refresh</a>.




## -see-also




<a href="https://msdn.microsoft.com/c4672df5-9e47-45f5-9504-1ebb0bf3c6a6">IAutomaticUpdatesSettings</a>



<a href="https://msdn.microsoft.com/308426d9-d524-406a-931c-1fdb854aa4fb">IAutomaticUpdatesSettings.Refresh</a>
 

 

