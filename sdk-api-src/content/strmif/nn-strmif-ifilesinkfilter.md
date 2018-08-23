---
UID: NN:strmif.IFileSinkFilter
title: IFileSinkFilter
author: windows-sdk-content
description: The IFileSinkFilter interface is implemented on filters that write media streams to a file.
old-location: dshow\ifilesinkfilter.htm
old-project: DirectShow
ms.assetid: aa1d3f8e-9790-4442-ba7e-896981bf1b96
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IFileSinkFilter, IFileSinkFilter interface [DirectShow], IFileSinkFilter interface [DirectShow],described, IFileSinkFilterInterface, dshow.ifilesinkfilter, strmif/IFileSinkFilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFileSinkFilter
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFileSinkFilter interface


## -description



The <code>IFileSinkFilter</code> interface is implemented on filters that write media streams to a file. A file sink filter in a video capture filter graph, for instance, writes the output of the video compression filter to a file. Typically, the application running this filter graph should enable the user to enter the name of the file to be written to. This interface enables the communication of this information.

If a filter needs the name of an output file, it should expose this interface to allow an application to set the file name. Note that there is currently no base class implementation of this interface.

Any application that must set the name of the file into which the file sink filter will write should use this interface to get and set the file name.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSinkFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFileSinkFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileSinkFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d635dfc-a3b3-4f75-8356-534a32156686">GetCurFile</a>
</td>
<td align="left" width="63%">
Retrieves the name of the current file into which media samples will be written.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d202be46-0a7a-4097-adf6-6ec9c6274449">SetFileName</a>
</td>
<td align="left" width="63%">
Sets the name of the file into which media samples will be written.

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/1339c441-2b10-461f-87f3-4835c1692740">IFileSinkFilter2</a> interface extends <b>IFileSinkFilter</b>.




## -see-also




<a href="https://msdn.microsoft.com/5efd174f-2eb1-44e6-97e3-b73c7c52fef1">Interfaces</a>
 

 

