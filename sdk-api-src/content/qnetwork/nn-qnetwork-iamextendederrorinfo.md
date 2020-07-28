---
UID: NN:qnetwork.IAMExtendedErrorInfo
title: IAMExtendedErrorInfo (qnetwork.h)
description: The IAMExtendedErrorInfo interface is used to obtain error information. Note  This interface is not implemented by any default components in DirectShow. .
helpviewer_keywords: ["IAMExtendedErrorInfo","IAMExtendedErrorInfo interface [DirectShow]","IAMExtendedErrorInfo interface [DirectShow]","described","IAMExtendedErrorInfoInterface","dshow.iamextendederrorinfo","qnetwork/IAMExtendedErrorInfo"]
old-location: dshow\iamextendederrorinfo.htm
tech.root: dshow
ms.assetid: 0e3274e6-7c22-4175-8b2e-cdf4afc1225e
ms.date: 12/05/2018
ms.keywords: IAMExtendedErrorInfo, IAMExtendedErrorInfo interface [DirectShow], IAMExtendedErrorInfo interface [DirectShow],described, IAMExtendedErrorInfoInterface, dshow.iamextendederrorinfo, qnetwork/IAMExtendedErrorInfo
f1_keywords:
- qnetwork/IAMExtendedErrorInfo
dev_langs:
- c++
req.header: qnetwork.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Qnetwork.h
api_name:
- IAMExtendedErrorInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMExtendedErrorInfo interface


## -description



The <code>IAMExtendedErrorInfo</code> interface is used to obtain error information. 


<div class="alert"><b>Note</b>  This interface is not implemented by any default components in DirectShow.</div>
<div> </div>





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMExtendedErrorInfo</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAMExtendedErrorInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMExtendedErrorInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamextendederrorinfo-get_errorcode">get_ErrorCode</a>
</td>
<td align="left" width="63%">
Retrieves the current error code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamextendederrorinfo-get_errordescription">get_ErrorDescription</a>
</td>
<td align="left" width="63%">
Retrieves the error description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamextendederrorinfo-get_haserror">get_HasError</a>
</td>
<td align="left" width="63%">
Queries whether an error occurred.

</td>
</tr>
</table> 


## -remarks



To define the interface identifier, include the header file Initguid.h before Qnetwork.h, but after Dshow.h and other header files:

<pre class="syntax" xml:space="preserve"><code>#include &lt;dshow.h&gt;
#include &lt;initguid.h&gt;
#include &lt;qnetwork.h&gt;
</code></pre>
<div class="alert"><b>Note</b>  Make sure that Initguid.h is included only once in your project. Otherwise, you will receive linker errors for duplicate GUID values.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 

