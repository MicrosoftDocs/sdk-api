---
UID: NN:wmsdkidl.IWMIStreamProps
title: IWMIStreamProps
author: windows-sdk-content
description: The IWMIStreamProps interface provides access to the properties of an IStream object.To obtain a pointer to an IWMIStreamProps interface, call IStream::QueryInterface.
old-location: wmformat\iwmistreamprops.htm
old-project: wmformat
ms.assetid: 336e11ce-6212-4d08-8c50-76b2128ddc35
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMIStreamProps, IWMIStreamProps interface [windows Media Format], IWMIStreamProps interface [windows Media Format],described, IWMIStreamPropsInterface, wmformat.iwmistreamprops, wmsdkidl/IWMIStreamProps
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMIStreamProps
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMIStreamProps interface


## -description



The <b>IWMIStreamProps</b> interface provides access to the properties of an <b>IStream</b> object.

To obtain a pointer to an <b>IWMIStreamProps</b> interface, call <b>IStream::QueryInterface</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMIStreamProps</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMIStreamProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMIStreamProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1873e20f-376a-45fe-ad02-0c28c894af18">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves a named property from the <b>IStream</b>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

