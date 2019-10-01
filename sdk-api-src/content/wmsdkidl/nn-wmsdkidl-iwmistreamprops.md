---
UID: NN:wmsdkidl.IWMIStreamProps
title: IWMIStreamProps (wmsdkidl.h)
author: windows-sdk-content
description: The IWMIStreamProps interface provides access to the properties of an IStream object.To obtain a pointer to an IWMIStreamProps interface, call IStream::QueryInterface.
old-location: wmformat\iwmistreamprops.htm
tech.root: wmformat
ms.assetid: 336e11ce-6212-4d08-8c50-76b2128ddc35
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMIStreamProps, IWMIStreamProps interface [windows Media Format], IWMIStreamProps interface [windows Media Format],described, IWMIStreamPropsInterface, wmformat.iwmistreamprops, wmsdkidl/IWMIStreamProps
ms.topic: interface
f1_keywords: 
 - "wmsdkidl/IWMIStreamProps"
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
 - IWMIStreamProps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMIStreamProps interface


## -description



The <b>IWMIStreamProps</b> interface provides access to the properties of an <b>IStream</b> object.

To obtain a pointer to an <b>IWMIStreamProps</b> interface, call <b>IStream::QueryInterface</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMIStreamProps</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMIStreamProps</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmistreamprops-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves a named property from the <b>IStream</b>.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

