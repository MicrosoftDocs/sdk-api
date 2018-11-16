---
UID: NN:sbe.IStreamBufferConfigure
title: IStreamBufferConfigure
author: windows-sdk-content
description: The IStreamBufferConfigure interface configures the location, number, and size of the backing files used by the various stream buffer objects.The StreamBufferConfig object exposes this interface.Before calling any of the Set methods on this interface, you must specify a registry key to hold the new settings. For more information, see IStreamBufferInitialize::SetHKEY.
old-location: mstv\istreambufferconfigure.htm
tech.root: mstv
ms.assetid: 8874fefd-2241-4b04-a7d5-191e13743fa0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IStreamBufferConfigure, IStreamBufferConfigure interface [Microsoft TV Technologies], IStreamBufferConfigure interface [Microsoft TV Technologies],described, IStreamBufferConfigureInterface, mstv.istreambufferconfigure, sbe/IStreamBufferConfigure
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Sbe.h
api_name:
 - IStreamBufferConfigure
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStreamBufferConfigure interface


## -description



The <b>IStreamBufferConfigure</b> interface configures the location, number, and size of the backing files used by the various stream buffer objects.

The <a href="https://msdn.microsoft.com/10678f33-2117-4add-8e4b-7b4d4eed11a9">StreamBufferConfig</a> object exposes this interface.

Before calling any of the <b>Set</b> methods on this interface, you must specify a registry key to hold the new settings. For more information, see <a href="https://msdn.microsoft.com/f8d85180-2575-4525-9b8a-bec354e2cd4c">IStreamBufferInitialize::SetHKEY</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferConfigure</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStreamBufferConfigure</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferConfigure</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bf2a99a-ed6b-4ce6-9190-756393afcef0">GetBackingFileCount</a>
</td>
<td align="left" width="63%">
Retrieves the maximum and minimum number of backing files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d02d87f-b617-4d46-82b2-41eb4b160d0f">GetBackingFileDuration</a>
</td>
<td align="left" width="63%">
Retrieves the backing file size, in seconds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb5d955d-11da-4ff3-990f-02c0c80d6405">GetDirectory</a>
</td>
<td align="left" width="63%">
Retrieves the directory where backing files are saved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c984ec40-22d0-4670-af7e-3c2ce611850f">SetBackingFileCount</a>
</td>
<td align="left" width="63%">
Sets the maximum and minimum number of backing files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1825896e-0e3c-4b89-8e0e-59faa0f8000d">SetBackingFileDuration</a>
</td>
<td align="left" width="63%">
Sets the backing file size, in seconds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff0604d4-bbcd-409e-8e3d-a132218dc3a9">SetDirectory</a>
</td>
<td align="left" width="63%">
Sets the directory where backing files are saved.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferConfigure)</code>.




## -see-also




<a href="https://msdn.microsoft.com/b3e8703a-2b69-4262-9aaa-ff9ac8ca2f28">Stream Buffer Engine Interfaces</a>
 

 

