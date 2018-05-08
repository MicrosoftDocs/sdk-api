---
UID: NN:medparam.IMediaParamInfo
title: IMediaParamInfo
author: windows-driver-content
description: The IMediaParamInfo interface retrieves information about the parameters that an object supports. The set of parameters that an object supports will not change over the lifetime of an application. To set parameter values, use the IMediaParams interface.
old-location: dshow\imediaparaminfo.htm
old-project: DirectShow
ms.assetid: 80c7da71-7898-4bda-a181-09ad8906532a
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IMediaParamInfo, IMediaParamInfo interface [DirectShow], IMediaParamInfo interface [DirectShow],described, IMediaParamInfoInterface, dshow.imediaparaminfo, medparam/IMediaParamInfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MP_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dmoguids.lib
-	Dmoguids.dll
api_name:
-	IMediaParamInfo
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMediaParamInfo interface


## -description



The <code>IMediaParamInfo</code> interface retrieves information about the parameters that an object supports. The set of parameters that an object supports will not change over the lifetime of an application. To set parameter values, use the <a href="https://msdn.microsoft.com/68ea8f6a-4b6d-4d79-a986-6032b767147b">IMediaParams</a> interface.




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
<a href="https://msdn.microsoft.com/b93b929c-c1a7-4e8e-93cf-118fcd6a3de9">GetCurrentTimeFormat</a>
</td>
<td align="left" width="63%">
Retrieves the current time format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c398554-af2b-4e7d-8f5c-1c361535e7c6">GetNumTimeFormats</a>
</td>
<td align="left" width="63%">
Retrieves the number of time formats that the object supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c518b8e-d5a7-40ba-9b10-4d23d4376890">GetParamCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of parameters that the object supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80fdb9c2-d979-4671-981a-54d968b23042">GetParamInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about a specified parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38ecde61-fd4a-4ba3-9cd4-d62a5aa55294">GetParamText</a>
</td>
<td align="left" width="63%">
Retrieves an array of text strings that describe the parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04e4c9ea-4570-4fd0-986b-c835c692b73b">GetSupportedTimeFormat</a>
</td>
<td align="left" width="63%">
Retrieves a supported time format.

</td>
</tr>
</table> 

