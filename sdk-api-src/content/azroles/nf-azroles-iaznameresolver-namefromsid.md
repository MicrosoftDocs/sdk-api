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

# IAzNameResolver::NameFromSid


## -description


The <b>NameFromSid</b> method gets the display name that corresponds to the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID).


## -parameters




### -param bstrSid [in]

The string representation of the SID to translate.


### -param pSidType [out]

An element of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556744">SID_NAME_USE</a> enumeration that specifies the type of SID being translated.


### -param pbstrName [out]

A pointer to the display name of the principal that corresponds to the SID specified by the <i>bstrSid</i> parameter.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. In particular, if the method cannot find the display name of the principal, it returns <b>CO_E_NOMATCHINGNAMEFOUND</b>. For a list of other common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



