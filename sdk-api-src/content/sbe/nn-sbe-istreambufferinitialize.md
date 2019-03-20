---
UID: NN:sbe.IStreamBufferInitialize
title: IStreamBufferInitialize (sbe.h)
author: windows-sdk-content
description: The IStreamBufferInitialize interface is used to configure the stream buffer filters. The Stream Buffer Source filter, Stream Buffer Sink filter, and StreamBufferConfig object all expose this interface.
old-location: mstv\istreambufferinitialize.htm
tech.root: mstv
ms.assetid: 357b2979-78de-4a99-bf52-4117af7dfaad
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IStreamBufferInitialize, IStreamBufferInitialize interface [Microsoft TV Technologies], IStreamBufferInitialize interface [Microsoft TV Technologies],described, IStreamBufferInitializeInterface, mstv.istreambufferinitialize, sbe/IStreamBufferInitialize
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
 - IStreamBufferInitialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStreamBufferInitialize interface


## -description



The <b>IStreamBufferInitialize</b> interface is used to configure the stream buffer filters. The <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filter, <a href="https://msdn.microsoft.com/e49fe3c2-e77f-419a-910c-78f72ebdfdbc">Stream Buffer Sink</a> filter, and <a href="https://msdn.microsoft.com/10678f33-2117-4add-8e4b-7b4d4eed11a9">StreamBufferConfig</a> object all expose this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferInitialize</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStreamBufferInitialize</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferInitialize</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8d85180-2575-4525-9b8a-bec354e2cd4c">SetHKEY</a>
</td>
<td align="left" width="63%">
Sets the registry key where the object stores configuration information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd25a967-9335-4bbd-ac85-f8b25f2be563">SetSIDs</a>
</td>
<td align="left" width="63%">
Sets the security identifiers (SIDs) that are used to protect access to the backing files.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferInitialize)</code>.




## -see-also




<a href="https://msdn.microsoft.com/b3e8703a-2b69-4262-9aaa-ff9ac8ca2f28">Stream Buffer Engine Interfaces</a>
 

 

