---
UID: NN:imapi2.IDiscFormat2Erase
title: IDiscFormat2Erase (imapi2.h)
author: windows-sdk-content
description: Use this interface to erase data from a disc.
old-location: imapi\idiscformat2erase.htm
tech.root: imapi
ms.assetid: 3789c876-f42c-4f69-b683-96c157d6418d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDiscFormat2Erase, IDiscFormat2Erase interface [IMAPI], IDiscFormat2Erase interface [IMAPI],described, imapi.idiscformat2erase, imapi2/IDiscFormat2Erase
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscFormat2Erase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiscFormat2Erase interface


## -description




Use this interface to erase data from a disc.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftDiscFormat2Erase) for the class identifier and __uuidof(IDiscFormat2Erase) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscFormat2Erase</b> interface inherits from <a href="https://msdn.microsoft.com/c0bc2e8b-bd60-4c97-bd86-41963b20b1a3">IDiscFormat2</a>. <b>IDiscFormat2Erase</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiscFormat2Erase</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc71d1bf-b068-42c0-a87d-ae8fac279a58">EraseMedia</a>
</td>
<td align="left" width="63%">
Erases the media in the active disc recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be52c76d-3c6a-44b7-a948-4d0b02a7a7bb">get_ClientName</a>
</td>
<td align="left" width="63%">
Retrieves the friendly name of the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6eda2c28-3dc6-4ca0-9806-0b9621bfe940">get_CurrentPhysicalMediaType</a>
</td>
<td align="left" width="63%">
Retrieves the type of media in the disc device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56b4db17-1699-4e09-9a6d-ef5e998621c5">get_FullErase</a>
</td>
<td align="left" width="63%">
Determines the quality of the disc erasure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f41ea99-e467-45ef-8f78-8b0637adf5be">get_Recorder</a>
</td>
<td align="left" width="63%">
Retrieves the recording device to use in the erase operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/641395b1-724b-42d1-b230-a4d6f3844077">put_ClientName</a>
</td>
<td align="left" width="63%">
Sets the friendly name of the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a76ebbe-69c5-46a4-b620-220957220e53">put_FullErase</a>
</td>
<td align="left" width="63%">
Determines the quality of the disc erasure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d38c0d75-eb9c-4b8c-bf0e-7f05eb2f5116">put_Recorder</a>
</td>
<td align="left" width="63%">
Sets the recording device to use in the erase operation.

</td>
</tr>
</table> 


## -remarks



To create the <b>MsftDiscFormat2Erase</b> object in a script, use IMAPI2.MsftDiscFormat2Erase as the program identifier when calling <b>CreateObject</b>.




## -see-also




<a href="https://msdn.microsoft.com/c0bc2e8b-bd60-4c97-bd86-41963b20b1a3">IDiscFormat2</a>
 

 

