---
UID: NN:oaidl.ICreateErrorInfo
title: ICreateErrorInfo
author: windows-sdk-content
description: Returns error information.
old-location: automat\icreateerrorinfo.htm
tech.root: automat
ms.assetid: 2e7c5ad5-9018-413e-8826-ef752ebf302c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICreateErrorInfo, ICreateErrorInfo interface [Automation], ICreateErrorInfo interface [Automation],described, _oa96_ICreateErrorInfo_Interface, automat.icreateerrorinfo, oaidl/ICreateErrorInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
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
 - oaidl.h
api_name:
 - ICreateErrorInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICreateErrorInfo interface


## -description


Returns error information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreateErrorInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICreateErrorInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICreateErrorInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32d10343-4be4-4ebc-b2fd-43a292c006b2">SetDescription</a>
</td>
<td align="left" width="63%">
Sets the textual description of the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7570ba3-d738-40d3-aefc-fbf6f4ca633e">SetGUID</a>
</td>
<td align="left" width="63%">
Sets the globally unique identifier (GUID) of the interface that defined the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c65f4bd-21ad-4118-bbe8-e2ff65b96213">SetHelpContext</a>
</td>
<td align="left" width="63%">
Sets the Help context identifier (ID) for the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb439d74-fd52-4c95-afc5-d57e2fe5029d">SetHelpFile</a>
</td>
<td align="left" width="63%">
Sets the path of the Help file that describes the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f0e6349-9d31-4ab6-9a91-3822e81188e5">SetSource</a>
</td>
<td align="left" width="63%">
Sets the language-dependent programmatic identifier (ProgID) for the class or application that raised the error.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c258677e-d53e-499d-a414-ce889709b23e">Error Handling Interfaces </a>
 

 

