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

# IWICComponentInfo::GetFriendlyName


## -description


Retrieves the component's friendly name, which is a human-readable display name for the component.


## -parameters




### -param cchFriendlyName [in]

Type: <b>UINT</b>

The size of the <i>wzFriendlyName</i> buffer.


### -param wzFriendlyName [in, out]

Type: <b>WCHAR*</b>

A pointer that receives the friendly name of the component.
               The locale of the string depends on the value that the codec wrote to the registry at install time. For built-in components, these strings are always in English.


### -param pcchActual [out]

Type: <b>UINT*</b>

A pointer that receives the actual length of the component's friendly name.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <i>cchFriendlyName</i> is 0 and <i>wzFriendlyName</i> is <b>NULL</b>, the required buffer size is returned in <i>pccchActual</i>.



