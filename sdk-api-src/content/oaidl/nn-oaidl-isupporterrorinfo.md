---
UID: NN:oaidl.ISupportErrorInfo
title: ISupportErrorInfo
author: windows-sdk-content
description: Ensures that error information can be propagated up the call chain correctly. Automation objects that use the error handling interfaces must implement ISupportErrorInfo.
old-location: automat\isupporterrorinfo.htm
old-project: automat
ms.assetid: 42d33066-36b4-4a5b-aa5d-46682e560f32
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ISupportErrorInfo, ISupportedErrorInfo, ISupportedErrorInfo interface [Automation], ISupportedErrorInfo interface [Automation],described, _oa96_ISupportErrorInfo_Interface, automat.isupporterrorinfo, oaidl/ISupportErrorInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: oaidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VARKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ISupportedErrorInfo
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# ISupportErrorInfo interface


## -description


Ensures that error information can be propagated up the call chain correctly. Automation objects that use the error handling interfaces must implement <b>ISupportErrorInfo</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISupportedErrorInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISupportErrorInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISupportedErrorInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a54ef18d-ee3f-4483-ac4a-99d758f0960a">InterfaceSupportsErrorInfo</a>
</td>
<td align="left" width="63%">
Indicates whether an interface supports the <a href="https://msdn.microsoft.com/4dda6909-2d9a-4727-ae0c-b5f90dcfa447">IErrorInfo</a> interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c258677e-d53e-499d-a414-ce889709b23e">Error Handling Interfaces </a>
 

 

