---
UID: NN:imapi2.DWriteEngine2Events
title: DWriteEngine2Events
author: windows-sdk-content
description: Implement this interface to receive notifications of the current write operation.
old-location: imapi\dwriteengine2events.htm
old-project: imapi
ms.assetid: 697f8247-6940-4b5e-8521-df89838837be
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: DWriteEngine2Events, DWriteEngine2Events interface [IMAPI], DWriteEngine2Events interface [IMAPI],described, imapi.dwriteengine2events, imapi2/DWriteEngine2Events
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - DWriteEngine2Events
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# DWriteEngine2Events interface


## -description


Implement this interface to receive notifications of the current write operation.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">DWriteEngine2Events</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>DWriteEngine2Events</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>DWriteEngine2Events</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927294">Update</a>
</td>
<td align="left" width="63%">
Implement this method to receive progress notification of the current write operation.

</td>
</tr>
</table> 

