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

# IAttachmentExecute::SetSource


## -description


Sets an alternate path or URL for the source of a file transfer.


## -parameters




### -param pszSource [in]

Type: <b>LPCWSTR</b>

A pointer to a string containing the path or URL to use as the source.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The path or URL declared here is used as the primary zone determinant. The policy under which the attachment is handled is based partially on the perceived zone. If <i>pszSource</i> is <b>NULL</b>, the default is Restricted Zone.

Calling <b>IAttachmentExecute::SetSource</b> is optional.

The path or URL declared here can also be used in the prompt UI as the <b>From</b> field.

The path or URL declared here can also be sent to handlers that can process URLs.



