---
UID: NF:oaidl.IDispatch.GetTypeInfo
title: IDispatch::GetTypeInfo
author: windows-sdk-content
description: Retrieves the type information for an object, which can then be used to get the type information for an interface.
old-location: automat\idispatch_gettypeinfo.htm
old-project: automat
ms.assetid: cc1ec9aa-6c40-4e70-819c-a7c6dd6b8c99
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetTypeInfo, GetTypeInfo method [Automation], GetTypeInfo method [Automation],IDispatch interface, GetTypeInfo method [Automation],IWebBrowser2 interface, IDispatch interface [Automation],GetTypeInfo method, IDispatch.GetTypeInfo, IDispatch::GetTypeInfo, IWebBrowser2 interface [Automation],GetTypeInfo method, IWebBrowser2::GetTypeInfo, _oa96_IDispatch::GetTypeInfo, automat.idispatch_gettypeinfo, oaidl/IDispatch::GetTypeInfo, oaidl/IWebBrowser2::GetTypeInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - Shdocvw.dll
api_name:
 - IDispatch.GetTypeInfo
 - IWebBrowser2.GetTypeInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IDispatch::GetTypeInfo


## -description


Retrieves the type information for an object, which can then be used to get the type information for an interface.


## -parameters




### -param iTInfo [in]

The type information to return. Pass 0 to retrieve type information for the <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> implementation.


### -param lcid [in]

The locale identifier for the type information. An object may be able to return different type information for different languages. This is important for classes that support localized member names. For classes that do not support localized member names, this parameter can be ignored.


### -param ppTInfo [out]

The requested type information object.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_BADINDEX
</b></dt>
</dl>
</td>
<td width="60%">
The <i>iTInfo</i> parameter was not 0.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/49b33ff9-f45c-4883-b31a-39e06b759b77">IWebBrowser2</a>
 

 

