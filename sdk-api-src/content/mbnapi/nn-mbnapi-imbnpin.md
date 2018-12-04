---
UID: NN:mbnapi.IMbnPin
title: IMbnPin
author: windows-sdk-content
description: Represents the device PIN.
old-location: mbn\imbnpin.htm
tech.root: mbn
ms.assetid: 76764dbb-7de0-4b95-a210-60b8e6a4b24b
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IMbnPin, IMbnPin interface [Microsoft Broadband Networks], IMbnPin interface [Microsoft Broadband Networks],described, mbn.imbnpin, mbnapi/IMbnPin
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnPin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnPin interface


## -description


Represents the device PIN.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnPin</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnPin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IMbnPin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf4fac68-65c8-456e-8381-e3f582fc836c">Change</a>
</td>
<td align="left" width="63%">
Changes the PIN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/612edeb9-3de4-48ac-a311-7238402e8658">Disable</a>
</td>
<td align="left" width="63%">
Disables a PIN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbdd767b-f08a-4e94-bccf-9ed0d1b4af29">Enable</a>
</td>
<td align="left" width="63%">
Enables a PIN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71bc0da9-af41-42d6-a7dc-91be54eb6f5c">Enter</a>
</td>
<td align="left" width="63%">
Enters a PIN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51957cb9-0204-4e07-aebf-1aaddb16b3c2">GetPinManager</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/b5cfabc7-81f8-4ea0-b6f4-5de011320f0b">IMbnPinManager</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e5ec24c-681c-4259-9f6a-949bf40d5b3e">Unblock</a>
</td>
<td align="left" width="63%">
Unblocks a blocked PIN.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnPin</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/146e5fa4-0883-47ca-9bf6-88cf4f4b5497">PinFormat</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The PIN format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c6918ada-4141-4b5e-88d8-c201a2b4a8a5">PinLengthMax</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The maximum length of the PIN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/09cfbe04-cfc4-4942-a78b-f97ef40f0d2c">PinLengthMin</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The minimum length of the PIN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d286c442-6878-4194-a605-40385a9789b9">PinMode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The PIN mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b80d552f-1900-4590-baa5-2fcdb9b32950">PinType</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
    The PIN type.

</td>
</tr>
</table> 


## -remarks



<b>IMbnPin</b> objects are provided by calls to the <a href="https://msdn.microsoft.com/21752fb9-db6b-4fd1-9c6f-a756408bda53">GetPin</a> and <a href="https://msdn.microsoft.com/732906dd-7d1e-49a1-a3cc-60075eed9c7c">GetPinList</a> methods of the <a href="https://msdn.microsoft.com/b5cfabc7-81f8-4ea0-b6f4-5de011320f0b">IMbnPinManager</a> interface.



