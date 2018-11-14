---
UID: NN:wmsdkidl.IWMReaderAdvanced5
title: IWMReaderAdvanced5
author: windows-sdk-content
description: The IWMReaderAdvanced5 interface enables you to associate a player-hook callback interface with the reader object.An IWMReaderAdvanced5 interface exists for every reader object.
old-location: wmformat\iwmreaderadvanced5.htm
tech.root: wmformat
ms.assetid: 28d697d8-99b5-4968-a765-ba01b86914f6
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMReaderAdvanced5, IWMReaderAdvanced5 interface [windows Media Format], IWMReaderAdvanced5 interface [windows Media Format],described, IWMReaderAdvanced5Interface, wmformat.iwmreaderadvanced5, wmsdkidl/IWMReaderAdvanced5
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMReaderAdvanced5
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderAdvanced5 interface


## -description



The <b>IWMReaderAdvanced5</b> interface enables you to associate a player-hook callback interface with the reader object.

An <b>IWMReaderAdvanced5</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface in the reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderAdvanced5</b> interface inherits from <a href="https://msdn.microsoft.com/56695c57-f6c5-4c57-b3d4-73d169b379fa">IWMReaderAdvanced4</a>. <b>IWMReaderAdvanced5</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderAdvanced5</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/499c6c31-8cdf-4b99-964a-1fd51c14c5bd">SetPlayerHook</a>
</td>
<td align="left" width="63%">
Sets the player hook callback interface that the reader calls before processing samples by using DirectX Video Acceleration.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -remarks



A player-hook callback can be assigned in the reader object to enable per-sample processing when using DirectX Video Acceleration.




## -see-also




<a href="https://msdn.microsoft.com/e995b707-d388-4ec3-b3c8-b111628c13d7">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/5d741e49-9fdf-4f8d-9ea1-faaecf879be4">IWMReaderAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/20bf3c00-0f35-4b8e-b78d-a36fbfd865b7">IWMReaderAdvanced3 Interface</a>



<a href="https://msdn.microsoft.com/56695c57-f6c5-4c57-b3d4-73d169b379fa">IWMReaderAdvanced4 Interface</a>



<a href="https://msdn.microsoft.com/95e8c151-9aae-4930-824c-8809dfc07705">IWMReaderAdvanced6 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

