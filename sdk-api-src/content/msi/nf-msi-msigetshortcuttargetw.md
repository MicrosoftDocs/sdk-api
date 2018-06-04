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

# MsiGetShortcutTargetW function


## -description


The 
<b>MsiGetShortcutTarget</b> function examines a shortcut and returns its product, feature name, and component if available.


## -parameters




### -param szShortcutPath

TBD


### -param szProductCode [out]

A GUID for the product code of the shortcut. This string buffer must be 39 characters long. The first 38 characters are for the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a>, and the last character is for the terminating null character. This parameter can be null.


### -param szFeatureId [out]

The feature name of the shortcut. The string buffer must be MAX_FEATURE_CHARS+1 characters long. This parameter can be null.


### -param szComponentCode [out]

A GUID of the component code. This string buffer must be 39 characters long. The first 38 characters are for the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a>, and the last character is for the terminating null character. This parameter can be null.


#### - szShortcutTarget [in]

A null-terminated string specifying the full path to a shortcut.


## -returns



This function returns UINT.




## -remarks



If the function fails, and the shortcut exists, the regular contents of the shortcut may be accessed through the 
<a href="_win32_ishelllink_cpp">IShellLink</a> interface.

Otherwise, the state of the target may be determined by using the 
<a href="database_functions.htm">Installer Selection Functions</a>.



