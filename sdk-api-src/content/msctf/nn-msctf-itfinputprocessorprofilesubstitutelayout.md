---
UID: NN:msctf.ITfInputProcessorProfileSubstituteLayout
title: ITfInputProcessorProfileSubstituteLayout (msctf.h)
author: windows-sdk-content
description: This interface is implemented by the TSF manager and is used by an application or text service to manipulate the substitute input locale identifier (keyboard layout) of a text service profile.
old-location: tsf\itfinputprocessorprofilesubstitutelayout.htm
tech.root: TSF
ms.assetid: e801ca27-4581-4369-886c-04b824d55013
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfileSubstituteLayout, ITfInputProcessorProfileSubstituteLayout interface [Text Services Framework], ITfInputProcessorProfileSubstituteLayout interface [Text Services Framework],described, msctf/ITfInputProcessorProfileSubstituteLayout, tsf.itfinputprocessorprofilesubstitutelayout
ms.topic: interface
f1_keywords: ["msctf/ITfInputProcessorProfileSubstituteLayout"]
req.header: msctf.h
req.include-header: Textstor.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfInputProcessorProfileSubstituteLayout
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfInputProcessorProfileSubstituteLayout interface


## -description


This  interface is implemented by the TSF manager and is used by an application or text service to manipulate the substitute input locale identifier (keyboard layout) of a text service profile. The interface ID is IID_ITfInputProcessorProfileSubstituteLayout.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfInputProcessorProfileSubstituteLayout</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfInputProcessorProfileSubstituteLayout</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfInputProcessorProfileSubstituteLayout</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofilesubstitutelayout-getsubstitutekeyboardlayout">GetSubstituteKeyboardLayout</a>
</td>
<td align="left" width="63%">
Retrieves the input locale identifier (keyboard layout).

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

