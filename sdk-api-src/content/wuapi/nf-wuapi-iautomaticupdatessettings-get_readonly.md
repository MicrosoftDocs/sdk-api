---
UID: NF:wuapi.IAutomaticUpdatesSettings.get_ReadOnly
title: IAutomaticUpdatesSettings::get_ReadOnly
author: windows-sdk-content
description: Gets a Boolean value that indicates whether the Automatic Update settings are read-only.
old-location: wua\iautomaticupdatessettings_readonly.htm
tech.root: Wua_Sdk
ms.assetid: e7a066b9-9581-4573-82e2-a6f2ca7440ac
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAutomaticUpdatesSettings interface [Windows Update Agent],ReadOnly property, IAutomaticUpdatesSettings.ReadOnly, IAutomaticUpdatesSettings.get_ReadOnly, IAutomaticUpdatesSettings::ReadOnly, IAutomaticUpdatesSettings::get_ReadOnly, ReadOnly property [Windows Update Agent], ReadOnly property [Windows Update Agent],IAutomaticUpdatesSettings interface, get_ReadOnly, wua.iautomaticupdatessettings_readonly, wuapi/IAutomaticUpdatesSettings::ReadOnly, wuapi/IAutomaticUpdatesSettings::get_ReadOnly
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IAutomaticUpdatesSettings.ReadOnly
 - IAutomaticUpdatesSettings.get_ReadOnly
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

