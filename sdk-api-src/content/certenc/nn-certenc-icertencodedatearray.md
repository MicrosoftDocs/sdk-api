---
UID: NN:certenc.ICertEncodeDateArray
title: ICertEncodeDateArray
author: windows-sdk-content
description: Provides methods for handling Date arrays used in certificate extensions.
old-location: security\icertencodedatearray.htm
old-project: seccrypto
ms.assetid: 9973c49a-d886-4cc4-b75e-7ff46f56d51c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICertEncodeDateArray, ICertEncodeDateArray interface [Security], ICertEncodeDateArray interface [Security],described, _certsrv_icertencodedatearray, certenc/ICertEncodeDateArray, security.icertencodedatearray
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certenc.h
req.include-header: Certsrv.h
req.redist: 
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
tech.root: 
req.typenames: X509EnrollmentAuthFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeDateArray
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# ICertEncodeDateArray interface


## -description


The <b>ICertEncodeDateArray</b> interface provides methods for handling <b>Date</b> arrays used in certificate extensions.

 A certificate extension can be created by using a <b>Date</b> array stored in an 
<a href="https://msdn.microsoft.com/a33ac417-b5f9-4ad7-a26e-13cdb1e4ac1b">extension handler</a> COM object instantiated by the policy module. Each element in the array is a <b>Date</b> value.

This interface is provided mainly as a demonstration for encoding custom extensions. The Certificate Services sample programs in the Platform Software Development Kit (SDK) contain source code for this interface.

<b>ICertEncodeDateArray</b> is defined in Certenc.h. When you create your program, however, use Certsrv.h as the include file. Certenc.dll provides the <b>ICertEncodeDateArray</b> interface. The type information for this interface is also in Certencl.dll, which is shipped with the Platform SDK.

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertEncodeDateArray</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICertEncodeDateArray</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertEncodeDateArray</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79937ef7-4b1a-4132-9ef4-23b2857c7fac">Decode</a>
</td>
<td align="left" width="63%">
Decodes an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1)-encoded <b>Date</b> array and stores the resulting array of <b>Date</b>s in the COM object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/102ca165-c320-4e18-986f-7375fbc617e0">Encode</a>
</td>
<td align="left" width="63%">
Performs ASN.1 encoding on a <b>Date</b> array stored in the COM object and returns the ASN.1-encoded <b>Date</b> array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25c61f42-b190-44c3-b2ba-57861bdfbce3">GetCount</a>
</td>
<td align="left" width="63%">
Returns the number of <b>Date</b> values in a <b>Date</b> array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db108b2a-c3ee-4ef8-be5c-74dc739dacee">GetValue</a>
</td>
<td align="left" width="63%">
Returns the <b>Date</b> value at a specified index of a <b>Date</b> array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f09087aa-ae10-4a59-9b59-5f8b72254ce6">Reset</a>
</td>
<td align="left" width="63%">
Resets a <b>Date</b> array to a specified number of elements and clears the values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e05a7aa1-81ad-4564-a6a5-65b8ac816598">SetValue</a>
</td>
<td align="left" width="63%">
Sets a <b>Date</b> value at a specified index of a <b>Date</b> array.

</td>
</tr>
</table> 

