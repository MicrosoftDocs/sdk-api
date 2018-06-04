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

# WslGetDistributionConfiguration function


## -description


   Retrieves the current configuration of a distribution registered with the Windows Subsystem for Linux (WSL).


## -parameters




### -param distributionName

TBD


### -param distributionVersion

TBD


### -param defaultUID

TBD


### -param wslDistributionFlags

TBD


### -param defaultEnvironmentVariables

TBD


### -param defaultEnvironmentVariableCount

TBD




#### - distroName [in]

Unique name representing a distribution (for example, "Fabrikam.Distro.10.01").


#### - pDefaultEnvironmentVariablesArray [out]

The address of a pointer to an array of default environment variable strings used when launching new WSL sessions for this distribution.


#### - pDefaultEnvironmentVariablesCount [out]

The number of elements in <i>pDefaultEnvironmentVariablesArray</i>.


#### - pDefaultUID [out]

The default user ID used when launching new WSL sessions for this distribution.


#### - pVersion [out]

The version of WSL for which this distribution is configured.


#### - pWslFlags [out]

The flags governing the behavior of this distribution.


## -returns



Returns S_OK on success, or a failing HRESULT otherwise.




## -remarks



The caller is responsible for freeing each string in <i>pDefaultEnvironmentVariablesArray</i> (and the array itself) via <b>CoTaskMemFree</b>.



