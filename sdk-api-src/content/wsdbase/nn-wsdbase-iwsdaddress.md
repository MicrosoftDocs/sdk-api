---
UID: NN:wsdbase.IWSDAddress
title: IWSDAddress
author: windows-sdk-content
description: Provides access to the individual components of a transport address.
old-location: ncd\iwsdaddress.htm
tech.root: WsdApi
ms.assetid: b19938b2-2fba-42fe-8c4e-5696c40acd58
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWSDAddress, IWSDAddress interface, IWSDAddress interface,described, ncd.iwsdaddress, wsdbase/IWSDAddress
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDAddress interface


## -description


Provides access to the individual components of a transport address.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDAddress</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDAddress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDAddress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a23ac1cd-d2af-4562-a623-64ca1deb1830">Deserialize</a>
</td>
<td align="left" width="63%">
Parses the address from the given buffer and retrieves the component parts of the address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6264a2f6-39db-4c55-a0b3-2705d2093d77">Serialize</a>
</td>
<td align="left" width="63%">
Serializes the address configuration into the specified buffer.

</td>
</tr>
</table> 

