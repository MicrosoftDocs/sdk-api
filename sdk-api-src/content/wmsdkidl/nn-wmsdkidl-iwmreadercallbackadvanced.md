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
<a href="https://msdn.microsoft.com/en-us/library/Dd743495(v=VS.85).aspx">AllocateForOutput</a>
</td>
<td align="left" width="63%">
Allocates a buffer for samples delivered to the <a href="https://msdn.microsoft.com/en-us/library/Dd743503(v=VS.85).aspx">IWMReaderCallback::OnSample</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743496(v=VS.85).aspx">AllocateForStream</a>
</td>
<td align="left" width="63%">
Allocates a buffer for samples delivered to the <a href="https://msdn.microsoft.com/en-us/library/Dd743500(v=VS.85).aspx">OnStreamSample</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743497(v=VS.85).aspx">OnOutputPropsChanged</a>
</td>
<td align="left" width="63%">
Called when the output media properties change because of an <a href="https://msdn.microsoft.com/en-us/library/Dd743605(v=VS.85).aspx">IWMReader::SetOutputProps</a> call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743500(v=VS.85).aspx">OnStreamSample</a>
</td>
<td align="left" width="63%">
Delivers stream samples from the source file without decompressing them first.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743501(v=VS.85).aspx">OnStreamSelection</a>
</td>
<td align="left" width="63%">
Notifies the application of stream changes made due to bandwidth restrictions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743502(v=VS.85).aspx">OnTime</a>
</td>
<td align="left" width="63%">
Notifies the application of the clock time the reader is working to. This is used when a user-provided clock has been specified.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757425(v=VS.85).aspx">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757429(v=VS.85).aspx">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743493(v=VS.85).aspx">IWMReaderCallback Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>



<a href="https://msdn.microsoft.com/e0aabe05-b317-42ac-85fc-5a75165722d4">Reading ASF Files</a>
 

 

