---
UID: NF:textstor.ITextStoreACP2.RetrieveRequestedAttrs
title: ITextStoreACP2::RetrieveRequestedAttrs
author: windows-sdk-content
description: Gets the attributes returned by a call to an attribute request method.
old-location: tsf\itextstoreacp2_retrieverequestedattrs.htm
tech.root: TSF
ms.assetid: fff22304-626e-4ae6-ac8c-f4a62ee823c2
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ITextStoreACP2 interface [Text Services Framework],RetrieveRequestedAttrs method, ITextStoreACP2.RetrieveRequestedAttrs, ITextStoreACP2::RetrieveRequestedAttrs, RetrieveRequestedAttrs, RetrieveRequestedAttrs method [Text Services Framework], RetrieveRequestedAttrs method [Text Services Framework],ITextStoreACP2 interface, textstor/ITextStoreACP2::RetrieveRequestedAttrs, tsf.itextstoreacp2_retrieverequestedattrs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - ITextStoreACP2.RetrieveRequestedAttrs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStoreACP2::RetrieveRequestedAttrs


## -description


Gets the attributes returned by a call to an attribute request method.


## -parameters




### -param ulCount [in]

Specifies the number of supported attributes to obtain.


### -param paAttrVals [out]

Pointer to the <a href="https://msdn.microsoft.com/9209ef60-6a1d-4aad-9f9f-775534116f37">TS_ATTRVAL</a> structure that receives the supported attributes. The members of this structure depend upon the <i>dwFlags</i> parameter of the calling method.


### -param pcFetched [out]

Receives the number of supported attributes.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c256f1c2-6b67-4417-8707-3490a2c5cb55">ITextStoreACP2</a>



<a href="https://msdn.microsoft.com/0eb663be-3e70-415b-89cd-7e5a0308e72a">RequestAttrsAtPosition</a>



<a href="https://msdn.microsoft.com/ff1cda58-f02d-4c39-aed5-ebacbef20780">RequestAttrsTransitioningAtPosition</a>



<a href="https://msdn.microsoft.com/ce26c2ec-f808-4f59-bc54-b3681b97ad89">RequestSupportedAttrs</a>



<a href="https://msdn.microsoft.com/9209ef60-6a1d-4aad-9f9f-775534116f37">TS_ATTRVAL</a>
 

 

