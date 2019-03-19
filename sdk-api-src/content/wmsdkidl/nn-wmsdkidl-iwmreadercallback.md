---
UID: NN:wmsdkidl.IWMReaderCallback
title: IWMReaderCallback (wmsdkidl.h)
author: windows-sdk-content
description: The IWMReaderCallback is implemented by the application to handle data being read from a file. A pointer to the interface is passed to IWMReader::Open.
old-location: wmformat\iwmreadercallback.htm
tech.root: wmformat
ms.assetid: 69b897a8-cc26-445d-9d41-b917b399fb14
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMReaderCallback, IWMReaderCallback interface [windows Media Format], IWMReaderCallback interface [windows Media Format],described, IWMReaderCallbackInterface, wmformat.iwmreadercallback, wmsdkidl/IWMReaderCallback
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
 - IWMReaderCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderCallback interface


## -description



The <b>IWMReaderCallback</b> is implemented by the application to handle data being read from a file. A pointer to the interface is passed to <a href="https://msdn.microsoft.com/en-us/library/Dd743597(v=VS.85).aspx">IWMReader::Open</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderCallback</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd798544(v=VS.85).aspx">IWMStatusCallback</a>. <b>IWMReaderCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743503(v=VS.85).aspx">OnSample</a>
</td>
<td align="left" width="63%">
Called during the reading of a file (due to a <a href="https://msdn.microsoft.com/en-us/library/Dd743608(v=VS.85).aspx">Start</a> call) indicating that new uncompressed data is available.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757425(v=VS.85).aspx">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757429(v=VS.85).aspx">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743494(v=VS.85).aspx">IWMReaderCallbackAdvanced Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798544(v=VS.85).aspx">IWMStatusCallback</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>



<a href="https://msdn.microsoft.com/e0aabe05-b317-42ac-85fc-5a75165722d4">Reading ASF Files</a>
 

 

