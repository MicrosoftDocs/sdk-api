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

# ICreateProcessInputs interface


## -description


Used by the <a href="https://msdn.microsoft.com/68B89E8C-2868-4F33-87A5-66A2FEFC0441">ICreatingProcess</a> interface to alter some parameters of the process that is being created.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreateProcessInputs</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICreateProcessInputs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICreateProcessInputs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07D9E07E-BDF8-46F7-AB75-A3041E96F1A1">AddCreateFlags</a>
</td>
<td align="left" width="63%">
 Set additional flags that will be included in the call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62270ED9-678B-4D39-BFF1-3F9E10AAF03A">AddStartupFlags</a>
</td>
<td align="left" width="63%">
 Additional flags that will be included in the <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure passed to <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6884E7A0-17E8-4F5F-B0A4-85BD3745ED12">GetCreateFlags</a>
</td>
<td align="left" width="63%">
Gets the additional flags that will be passed to <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B929D77A-FEE4-40A1-8B40-34E2E73048F9">SetCreateFlags</a>
</td>
<td align="left" width="63%">
 Set the flags that will be included in the call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5898B21B-5D3B-4950-9DB4-5B7FD19C9187">SetEnvironmentVariable</a>
</td>
<td align="left" width="63%">
Sets a variable in the environment of the created process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B54934CA-6345-4B06-BA5F-75FA4B5CEE4F">SetHotKey</a>
</td>
<td align="left" width="63%">
Sets the hot key for the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BFCDC5B1-740E-4CE9-8E06-75F3ECA7B7E6">SetTitle</a>
</td>
<td align="left" width="63%">
 Sets the title that will be passed <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>.

</td>
</tr>
</table> 


## -remarks



Applications do not implement this interface.

A pointer to this interface is passed to <a href="https://msdn.microsoft.com/5A13ABDB-8453-41BE-AF0C-B5A07486CBE6">ICreatingProcess::OnCreating</a>.



