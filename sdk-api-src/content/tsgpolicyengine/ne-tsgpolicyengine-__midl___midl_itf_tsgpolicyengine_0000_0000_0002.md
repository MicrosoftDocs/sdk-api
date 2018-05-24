---
UID: NE:tsgpolicyengine.__MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0002
title: "__MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0002"
author: windows-driver-content
description: Specifies the type of event that the ITSGAccountingEngine::DoAccounting method is being notified of.
old-location: termserv\aaaccountingdatatype.htm
old-project: TermServ
ms.assetid: 2864d044-266c-44e4-90d3-ccd75bf08348
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: AAAccountingDataType, AAAccountingDataType enumeration [Remote Desktop Services], AA_MAIN_SESSION_CLOSED, AA_MAIN_SESSION_CREATION, AA_SUB_SESSION_CLOSED, AA_SUB_SESSION_CREATION, __MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0002, termserv.aaaccountingdatatype, tsgpolicyengine/AAAccountingDataType, tsgpolicyengine/AA_MAIN_SESSION_CLOSED, tsgpolicyengine/AA_MAIN_SESSION_CREATION, tsgpolicyengine/AA_SUB_SESSION_CLOSED, tsgpolicyengine/AA_SUB_SESSION_CREATION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: tsgpolicyengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSGPolicyEngine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AAAccountingDataType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tsgpolicyengine.h
-	TSGPolicyEngine.h
api_name:
-	AAAccountingDataType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

