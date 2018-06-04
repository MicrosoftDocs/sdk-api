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

# SLIsGenuineLocalEx function


## -description


Checks whether the specified application installation is genuine.


## -parameters




### -param pAppId [in]

A pointer to an <b>SLID</b> structure that specifies the application to check.


### -param pSkuId [in, optional]

A pointer to an <b>SLID</b> structure that specifies the SKU of the application to check.

If this parameter is not <b>NULL</b>, this function uses the value of this parameter instead of the value of the <i>pAppId</i> parameter to check whether the application installation is genuine. If the SKU license contains a <b>ProductUniquenessGroupId</b>  value, that value is also used to check whether the application is genuine.


### -param pGenuineState [out]

A pointer to a value of the <a href="https://msdn.microsoft.com/3be69be1-289c-466a-9271-5309fd1319fe">SL_GENUINE_STATE</a> enumeration that specifies the state of the installation.  This function does not change the value of this parameter if the return value is any value other than <b>S_OK</b>.

If this parameter is <b>NULL</b>, the function fails with a return value of <b>E_INVALIDARG</b>.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This function checks the <b>Tampered</b> flag of the license associated with the specified application and the SKU, if specified. If the license is not valid, or if the <b>Tampered</b> flag of either license is set, the installation is not considered genuine.



