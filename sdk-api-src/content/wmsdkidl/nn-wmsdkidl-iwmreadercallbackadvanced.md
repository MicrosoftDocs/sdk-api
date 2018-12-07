---
UID: NN:wmsdkidl.IWMReaderCallbackAdvanced
title: IWMReaderCallbackAdvanced
author: windows-sdk-content
description: The IWMReaderCallback interface is implemented by the application to handle data being read from a file.
old-location: wmformat\iwmreadercallbackadvanced.htm
tech.root: wmformat
ms.assetid: 9d18961a-5ea4-4f3e-b473-7399e155f800
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMReaderCallbackAdvanced, IWMReaderCallbackAdvanced interface [windows Media Format], IWMReaderCallbackAdvanced interface [windows Media Format],described, IWMReaderCallbackAdvancedInterface, wmformat.iwmreadercallbackadvanced, wmsdkidl/IWMReaderCallbackAdvanced
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
 - IWMReaderCallbackAdvanced
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderCallbackAdvanced interface


## -description



The <b>IWMReaderCallback</b> interface is implemented by the application to handle data being read from a file.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderCallbackAdvanced</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMReaderCallbackAdvanced</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderCallbackAdvanced</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd7340c9-9380-4dba-b8ac-2a616ce9949f">AllocateForOutput</a>
</td>
<td align="left" width="63%">
Allocates a buffer for samples delivered to the <a href="https://msdn.microsoft.com/0f6e4d4f-4295-44ff-95bc-e683bdbab8e0">IWMReaderCallback::OnSample</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82d31f4b-d8a8-4538-be5e-dd9149e3f420">AllocateForStream</a>
</td>
<td align="left" width="63%">
Allocates a buffer for samples delivered to the <a href="https://msdn.microsoft.com/6bfdd903-a3a4-4ef4-b88a-4d24c9c0f4b8">OnStreamSample</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e8193c4-5fc7-4b19-9f6e-6873ebe5156a">OnOutputPropsChanged</a>
</td>
<td align="left" width="63%">
Called when the output media properties change because of an <a href="https://msdn.microsoft.com/0a5325d1-880b-4d65-96af-9d311dca989b">IWMReader::SetOutputProps</a> call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6bfdd903-a3a4-4ef4-b88a-4d24c9c0f4b8">OnStreamSample</a>
</td>
<td align="left" width="63%">
Delivers stream samples from the source file without decompressing them first.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0d699b3-e2f3-427c-9159-e2ed875887ca">OnStreamSelection</a>
</td>
<td align="left" width="63%">
Notifies the application of stream changes made due to bandwidth restrictions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9913bbc4-df59-484f-b050-324e2ecdeb1c">OnTime</a>
</td>
<td align="left" width="63%">
Notifies the application of the clock time the reader is working to. This is used when a user-provided clock has been specified.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e995b707-d388-4ec3-b3c8-b111628c13d7">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/69b897a8-cc26-445d-9d41-b917b399fb14">IWMReaderCallback Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>



<a href="https://msdn.microsoft.com/e0aabe05-b317-42ac-85fc-5a75165722d4">Reading ASF Files</a>
 

 

