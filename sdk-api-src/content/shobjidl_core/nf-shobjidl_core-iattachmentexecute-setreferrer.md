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

# IAttachmentExecute::SetReferrer


## -description


Sets the security zone associated with the attachment file based on the referring file.


## -parameters




### -param pszReferrer [in]

Type: <b>LPCWSTR</b>

A pointer to a string containing the path of the referring file.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IAttachmentExecute::SetReferrer</b> and <a href="https://msdn.microsoft.com/6545252b-1c43-4d62-9784-b63688ef9fdc">IAttachmentExecute::SetSource</a> have similar functionality. If both are set, the least-trusted zone of the two is used.

<b>IAttachmentExecute::SetReferrer</b> is used by container files to indicate indirect inheritance and avoid zone elevation. It can also be used with shortcut files to limit elevation based on parameters.

Calling <b>IAttachmentExecute::SetReferrer</b> is optional.

<b>IAttachmentExecute::SetReferrer</b> is only used to determine the security zone and its associated policies.



