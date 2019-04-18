---
UID: NN:medparam.IMediaParamInfo
title: IMediaParamInfo (medparam.h)
author: windows-sdk-content
description: The IMediaParamInfo interface retrieves information about the parameters that an object supports. The set of parameters that an object supports will not change over the lifetime of an application. To set parameter values, use the IMediaParams interface.
old-location: dshow\imediaparaminfo.htm
tech.root: DirectShow
ms.assetid: 80c7da71-7898-4bda-a181-09ad8906532a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMediaParamInfo, IMediaParamInfo interface [DirectShow], IMediaParamInfo interface [DirectShow],described, IMediaParamInfoInterface, dshow.imediaparaminfo, medparam/IMediaParamInfo
ms.topic: interface
req.header: medparam.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaParamInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaParamInfo interface


## -description



The <code>IMediaParamInfo</code> interface retrieves information about the parameters that an object supports. The set of parameters that an object supports will not change over the lifetime of an application. To set parameter values, use the <a href="https://msdn.microsoft.com/en-us/library/Dd406971(v=VS.85).aspx">IMediaParams</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaParamInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMediaParamInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaParamInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406965(v=VS.85).aspx">GetCurrentTimeFormat</a>
</td>
<td align="left" width="63%">
Retrieves the current time format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406966(v=VS.85).aspx">GetNumTimeFormats</a>
</td>
<td align="left" width="63%">
Retrieves the number of time formats that the object supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406967(v=VS.85).aspx">GetParamCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of parameters that the object supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406968(v=VS.85).aspx">GetParamInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about a specified parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406969(v=VS.85).aspx">GetParamText</a>
</td>
<td align="left" width="63%">
Retrieves an array of text strings that describe the parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406970(v=VS.85).aspx">GetSupportedTimeFormat</a>
</td>
<td align="left" width="63%">
Retrieves a supported time format.

</td>
</tr>
</table> 

