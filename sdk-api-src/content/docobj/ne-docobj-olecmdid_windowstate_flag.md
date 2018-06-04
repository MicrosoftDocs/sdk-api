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

# OLECMDID_WINDOWSTATE_FLAG enumeration


## -description


Specifies the window state.


## -enum-fields




### -field OLECMDIDF_WINDOWSTATE_USERVISIBLE

The window is visible.


### -field OLECMDIDF_WINDOWSTATE_ENABLED

The window has focus.


### -field OLECMDIDF_WINDOWSTATE_USERVISIBLE_VALID

The window is visible and valid.


### -field OLECMDIDF_WINDOWSTATE_ENABLED_VALID

The window has focus and is valid.


## -remarks



A value from this enumeration is passed as the <i>nCmdExecOpt</i> parameter to <a href="https://msdn.microsoft.com/a2071ca9-8675-4f53-b30e-8c7198c2acca">IOleCommandTarget::Exec</a> in conjunction with passing the OLECMDID_WINDOWSTATECHANGED value of the <a href="https://msdn.microsoft.com/ae1592b6-2afd-4379-a18e-d46b226bc9e2">OLECMDID</a> enumeration as the <i>nCmdID</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/ae1592b6-2afd-4379-a18e-d46b226bc9e2">OLECMDID</a>
 

 

