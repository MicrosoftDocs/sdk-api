---
UID: NN:imapi2.IBurnVerification
title: IBurnVerification (imapi2.h)
author: windows-sdk-content
description: Use this interface with IDiscFormat2Data or IDiscFormat2TrackAtOnce to get or set the Burn Verification Level property which dictates how burned media is verified for integrity after the write operation.
old-location: imapi\iburnverification.htm
tech.root: imapi
ms.assetid: 3a410ab8-dfc3-4c30-a198-3888ed750a6d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBurnVerification, IBurnVerification interface [IMAPI], IBurnVerification interface [IMAPI],described, imapi.iburnverification, imapi2/IBurnVerification
ms.topic: interface
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - IBurnVerification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBurnVerification interface


## -description


Use  this interface with  <a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a> or <a href="https://msdn.microsoft.com/27f2d248-1c83-4784-82f9-75ce0a038b87">IDiscFormat2TrackAtOnce</a> to get or set the Burn Verification Level property which dictates how burned media is verified for integrity after the write operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBurnVerification</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBurnVerification</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBurnVerification</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4be9191a-8f87-4571-a7b6-60d582ec471d">get_BurnVerificationLevel</a>
</td>
<td align="left" width="63%">
Retrieves the current Burn Verification Level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71842038-91dc-4de5-8169-3bc97ef288c6">put_BurnVerificationLevel</a>
</td>
<td align="left" width="63%">
Sets the  Burn Verification Level.

</td>
</tr>
</table> 


## -remarks



The following example function demonstrates how the burn verification level defined by <a href="https://msdn.microsoft.com/83a267b7-8b25-49b8-b1d0-83efbad8fa2a">IMAPI_BURN_VERIFICATION_LEVEL</a>, can be implemented. Burn verification level should be set prior to a burn operation.


```cpp
#include <imapi2.h>

HRESULT setBurnVerification(
    IDiscFormat2Data                *DataWriter,
    IMAPI_BURN_VERIFICATION_LEVEL   VerificationLevel
    )

{
    HRESULT hr = S_OK;
    IBurnVerification *burnVerifier = NULL;
 
    hr = DataWriter->QueryInterface(IID_PPV_ARGS(&burnVerifier));
 
    if (SUCCEEDED(hr))
    {
        hr = burnVerifier->put_BurnVerificationLevel(VerificationLevel);
    }
 
    if (burnVerifier != NULL)
    {
        burnVerifier->Release();
        burnVerifier = NULL;
    }
 
    return hr;
}

```


This interface is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>



<a href="https://msdn.microsoft.com/27f2d248-1c83-4784-82f9-75ce0a038b87">IDiscFormat2TrackAtOnce</a>



<a href="https://msdn.microsoft.com/83a267b7-8b25-49b8-b1d0-83efbad8fa2a">IMAPI_BURN_VERIFICATION_LEVEL</a>
 

 

