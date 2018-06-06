---
UID: NF:combaseapi.CoCopyProxy
title: CoCopyProxy function
author: windows-sdk-content
description: Makes a private copy of the specified proxy.
old-location: com\cocopyproxy.htm
old-project: com
ms.assetid: 26de7bac-8745-40c0-be0a-dcec88a3ecaf
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: CoCopyProxy, CoCopyProxy function [COM], _com_CoCopyProxy, com.cocopyproxy, combaseapi/CoCopyProxy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
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
req.typenames: REGCLS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoCopyProxy
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# CoCopyProxy function


## -description


Makes a private copy of the specified proxy.


## -parameters




### -param pProxy [in]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on the proxy to be copied. This parameter cannot be <b>NULL</b>.


### -param ppCopy [out]

Address of the pointer variable that receives the interface pointer to the copy of the proxy. This parameter cannot be <b>NULL</b>.


## -returns



This function can return the following values.

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
Indicates success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are invalid.

</td>
</tr>
</table>
 




## -remarks



<b>CoCopyProxy</b> makes a private copy of the specified proxy. Typically, this function is called when a client needs to change the authentication information of its proxy through a call to either <a href="https://msdn.microsoft.com/c2e5e681-8fa5-4b02-b59d-ba796eb0dccf">CoSetProxyBlanket</a> or <a href="https://msdn.microsoft.com/adb35089-2846-4782-8c96-d3d1e14beed9">IClientSecurity::SetBlanket</a> without changing this information for other clients. <b>CoSetProxyBlanket</b> affects all the users of an instance of a proxy, so creating a private copy of the proxy through a call to <b>CoCopyProxy</b> and then calling <b>CoSetProxyBlanket</b> (or <b>IClientSecurity::SetBlanket</b>) using the copy eliminates the problem.

This helper function encapsulates the following sequence of common calls (error handling excluded):



<pre class="syntax" xml:space="preserve"><code>    pProxy-&gt;QueryInterface(IID_IClientSecurity, (void**)&amp;pcs);
    pcs-&gt;CopyProxy(punkProxy, ppunkCopy);
    pcs-&gt;Release();
</code></pre>
Local interfaces may not be copied. <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> and <a href="https://msdn.microsoft.com/65066913-f9d8-48c7-bcb5-68c8ddc4a009">IClientSecurity</a> are examples of existing local interfaces.

Copies of the same proxy have a special relationship with respect to <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a>. Given a proxy, a, of the IA interface of a remote object, suppose a copy of a is created, called b. In this case, calling <b>QueryInterface</b> from the b proxy for IID_IA will not retrieve the IA interface on b, but the one on a, the original proxy with the "default" security settings for the IA interface.




## -see-also




<a href="https://msdn.microsoft.com/c2e5e681-8fa5-4b02-b59d-ba796eb0dccf">CoSetProxyBlanket</a>



<a href="https://msdn.microsoft.com/adb35089-2846-4782-8c96-d3d1e14beed9">IClientSecurity::SetBlanket</a>



<a href="https://msdn.microsoft.com/c9f6d06c-da24-48ea-908a-2462c33f7ee3">Security in COM</a>
 

 

