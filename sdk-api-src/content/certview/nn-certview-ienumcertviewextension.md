---
UID: NN:certview.IEnumCERTVIEWEXTENSION
title: IEnumCERTVIEWEXTENSION
author: windows-sdk-content
description: Represents an extension-enumeration sequence that contains the certificate extension data for the current row of the row-enumeration sequence.
old-location: security\ienumcertviewextension.htm
old-project: seccrypto
ms.assetid: d5acff51-06f8-4a6f-aa9e-97ba052b1b34
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnumCERTVIEWEXTENSION, IEnumCERTVIEWEXTENSION interface [Security], IEnumCERTVIEWEXTENSION interface [Security],described, _certsrv_ienumcertviewextension, certview/IEnumCERTVIEWEXTENSION, security.ienumcertviewextension
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certview.h
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
req.typenames: ENUM_CATYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IEnumCERTVIEWEXTENSION
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
---

# IEnumCERTVIEWEXTENSION interface


## -description


The <b>IEnumCERTVIEWEXTENSION</b> interface represents an extension-enumeration sequence that contains the  certificate extension data for the current row of the row-enumeration sequence.

 The extension-enumeration sequence is obtained by a call to the   
<a href="https://msdn.microsoft.com/41028000-fa87-4ad0-93fc-314c5d3870f9">IEnumCERTVIEWROW::EnumCertViewExtension</a> method. After this enumeration sequence is obtained, the methods of the <b>IEnumCERTVIEWEXTENSION</b> interface can be used to perform the following tasks:<ul>
<li>Navigate the extension-enumeration sequence.</li>
<li>Retrieve the name, value, and flags of the extension in the enumeration.</li>
<li>Clone an exact copy of the extension-enumeration sequence.</li>
</ul>


<b>IEnumCERTVIEWEXTENSION</b> is defined in Certview.h. When you create your program, however, use Certsrv.h as the include file. Certadm.dll provides the <b>IEnumCERTVIEWEXTENSION</b> interface. The type information for this interface is also in Certadml.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumCERTVIEWEXTENSION</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IEnumCERTVIEWEXTENSION</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumCERTVIEWEXTENSION</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b8e19e4-459f-45f0-abb6-e1e0e115e0f5">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the extension-enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c175eba9-ea7c-4018-876a-2db732cb57c4">GetFlags</a>
</td>
<td align="left" width="63%">
Retrieves the policy and origin flags of the current extension in the extension-enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c56708c-ae25-46f5-94f3-d58eea8d08d4">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the current extension in the extension-enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a81b096-36ba-416a-ad15-5bf1c4d512dd">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves the value of the current extension in the extension-enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/658daf9d-0f61-4c93-9688-a7c74464ca89">Next</a>
</td>
<td align="left" width="63%">
Moves to the next extension in the extension-enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7af29b1f-5b43-4ab7-81fa-d03e065f014f">Reset</a>
</td>
<td align="left" width="63%">
Moves to the beginning of the extension-enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b354cf0e-2f15-42a5-8e84-4db9bc4e6a8d">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of extensions in the extension-enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/41028000-fa87-4ad0-93fc-314c5d3870f9">IEnumCERTVIEWROW::IEnumCertViewExtension</a>
 

 

