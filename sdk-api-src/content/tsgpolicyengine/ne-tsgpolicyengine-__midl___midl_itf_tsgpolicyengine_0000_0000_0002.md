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

# __MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0002 enumeration


## -description


Specifies the type of event that the <a href="https://msdn.microsoft.com/ebc57caa-804b-46a4-96bb-8b50c13029ab">ITSGAccountingEngine::DoAccounting</a> method is being notified of.


## -enum-fields




### -field AA_MAIN_SESSION_CREATION

A new session was created.

The following fields in the <a href="https://msdn.microsoft.com/1c79f910-8dd9-47dc-80d1-f6252f0a43dd">AAAccountingData</a> structure represented by the <i>accountingData</i> parameter are valid:

<ul>
<li><b>userName</b></li>
<li><b>clientName</b></li>
<li><b>authType</b></li>
<li><b>mainSessionId</b></li>
</ul>

### -field AA_SUB_SESSION_CREATION

A new subsession was created by an  existing connection.

The following fields in the <a href="https://msdn.microsoft.com/1c79f910-8dd9-47dc-80d1-f6252f0a43dd">AAAccountingData</a> structure represented by the <i>accountingData</i> parameter are valid:

<ul>
<li><b>userName</b></li>
<li><b>resourceName</b></li>
<li><b>portNumber</b></li>
<li><b>protocolName</b></li>
<li><b>mainSessionId</b></li>
<li><b>subSessionId</b></li>
</ul>

### -field AA_SUB_SESSION_CLOSED

A subsession was closed.

The following fields in the <a href="https://msdn.microsoft.com/1c79f910-8dd9-47dc-80d1-f6252f0a43dd">AAAccountingData</a> structure represented by the <i>accountingData</i> parameter are valid:

<ul>
<li><b>numberOfBytesTransfered</b></li>
<li><b>numberOfBytesReceived</b></li>
<li><b>mainSessionId</b></li>
<li><b>subSessionId</b></li>
</ul>

### -field AA_MAIN_SESSION_CLOSED

A connection was closed.

The following fields in the <a href="https://msdn.microsoft.com/1c79f910-8dd9-47dc-80d1-f6252f0a43dd">AAAccountingData</a> structure represented by the <i>accountingData</i> parameter are valid:

<ul>
<li><b>mainSessionId</b></li>
</ul>

## -see-also




<a href="https://msdn.microsoft.com/ebc57caa-804b-46a4-96bb-8b50c13029ab">ITSGAccountingEngine::DoAccounting</a>
 

 

