---
UID: NN:certenc.ICertEncodeStringArray
title: ICertEncodeStringArray
author: windows-sdk-content
description: Provides methods for handling string arrays used in certificate extensions.
old-location: security\icertencodestringarray.htm
tech.root: seccrypto
ms.assetid: 5515c25e-f788-4222-8f66-f5d86bd2a3a3
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ICertEncodeStringArray, ICertEncodeStringArray interface [Security], ICertEncodeStringArray interface [Security],described, _certsrv_icertencodestringarray, certenc/ICertEncodeStringArray, security.icertencodestringarray
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certenc.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeStringArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeStringArray interface


## -description


The <b>ICertEncodeStringArray</b> interface provides methods for handling string arrays used in certificate extensions.

 A certificate extension can be created by using a string array stored in an 
<a href="https://msdn.microsoft.com/fb106cab-8a61-4a83-8fb4-7c045d905575">extension handler</a> COM object instantiated by the policy module. Each element in the array is a string value.

This interface is provided mainly as a demonstration for encoding custom extensions. The Certificate Services sample programs in the Platform Software Development Kit (SDK) contain source code for this interface.

<b>ICertEncodeStringArray</b> is defined in Certenc.h. When you create your program, however, use Certsrv.h as the include file. Certenc.dll provides the <b>ICertEncodeStringArray</b> interface. The type information for this interface is also in Certencl.dll, which is shipped with the Platform SDK.

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertEncodeStringArray</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICertEncodeStringArray</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertEncodeStringArray</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35799b54-2c04-4bb4-a227-d2902b2379ec">Decode</a>
</td>
<td align="left" width="63%">
Decodes an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1)-encoded string array and stores the resulting array of strings in the COM object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8fc51ea-4d83-402a-a4ac-ce55d385905c">Encode</a>
</td>
<td align="left" width="63%">
Performs ASN.1 encoding on a string array stored in the COM object and returns the ASN.1-encoded string array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c02a23ea-87c2-4458-8b1a-b010e8103a90">GetCount</a>
</td>
<td align="left" width="63%">
Returns the number of values in a string array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7020f364-4f92-46b8-a8e8-360d8e0fa051">GetStringType</a>
</td>
<td align="left" width="63%">
Returns the type of values contained in a string array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93f827c6-4dc6-462f-8865-eb631d7fe7bc">GetValue</a>
</td>
<td align="left" width="63%">
Returns the value at a specified index of a string array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/125524ae-236d-4507-9c00-76a016bf6c62">Reset</a>
</td>
<td align="left" width="63%">
Resets a string array to a specified type and number of elements, and clears the values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41e5c2b8-a0da-426a-b411-0bdc3fd7ecfe">SetValue</a>
</td>
<td align="left" width="63%">
Sets a value at a specified index of a string array.

</td>
</tr>
</table> 

