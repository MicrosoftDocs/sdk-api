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

# SHRegGetBoolValueFromHKCUHKLM function


## -description


<p class="CCE_Message">[This function is no longer supported.]

Evaluates a registry key value and returns a boolean value that reflects whether the value exists and the expected state matches the actual state. This function will first check HKEY_CURRENT_USER for the requested information in the specified subkey. If the information does not exist under the HKEY_CURRENT_USER subtree it will check the HKEY_LOCAL_MACHINE subtree for the same information.

            


## -parameters




### -param pszKey

Type: <b>PCWSTR</b>

A pointer to a null-terminated Unicode string that specifies the path to the key to be checked.


### -param pszValue [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated Unicode string that specifies the value to be evaluated.


### -param fDefault [in]

Type: <b>BOOL</b>

The expected state of the evaluation, as defined by the calling function.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if the evaluation matches the <i>fDefault</i> value; otherwise, <b>FALSE</b>.



