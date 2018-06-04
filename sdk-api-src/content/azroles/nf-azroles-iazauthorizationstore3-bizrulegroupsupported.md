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

# IAzAuthorizationStore3::BizruleGroupSupported


## -description


The <b>BizruleGroupSupported</b> method returns a Boolean value that specifies whether this <a href="https://msdn.microsoft.com/7063416c-b132-4b3a-bb2b-d27fccea25e4">IAzAuthorizationStore3</a> object supports application groups that use business rule (BizRule) scripts.


## -parameters




### -param pbSupported [out]

<b>VARIANT_TRUE</b> if the current <a href="https://msdn.microsoft.com/7063416c-b132-4b3a-bb2b-d27fccea25e4">IAzAuthorizationStore3</a> object supports scripts that use business logic to determine group membership; otherwise, <b>VARIANT_FALSE</b>.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



