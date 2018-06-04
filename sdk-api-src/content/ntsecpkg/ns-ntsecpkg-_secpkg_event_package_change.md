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

# _SECPKG_EVENT_PACKAGE_CHANGE structure


## -description


The <b>SECPKG_EVENT_PACKAGE_CHANGE</b> structure contains information about changes in <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> availability. This structure is indirectly used by the 
<a href="https://msdn.microsoft.com/689a1956-5eab-4eec-93ef-5ddcef6546ee">RegisterNotification</a> function. It is returned to a registered notification function when the function is registered to receive notifications for the <i>NotificationClass</i> parameter value NOTIFY_CLASS_PACKAGE_CHANGE.


## -struct-fields




### -field ChangeType

The type of change. One of the following values will be specified.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_PACKAGE_CHANGE_LOAD"></a><a id="secpkg_package_change_load"></a><dl>
<dt><b>SECPKG_PACKAGE_CHANGE_LOAD</b></dt>
</dl>
</td>
<td width="60%">
A package was loaded.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_PACKAGE_CHANGE_UNLOAD"></a><a id="secpkg_package_change_unload"></a><dl>
<dt><b>SECPKG_PACKAGE_CHANGE_UNLOAD</b></dt>
</dl>
</td>
<td width="60%">
A package was unloaded.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_PACKAGE_CHANGE_SELECT"></a><a id="secpkg_package_change_select"></a><dl>
<dt><b>SECPKG_PACKAGE_CHANGE_SELECT</b></dt>
</dl>
</td>
<td width="60%">
A new package became the preferred security package.

</td>
</tr>
</table>
 


### -field PackageId

The identifier of the security package.


### -field PackageName

The name of the security package.

