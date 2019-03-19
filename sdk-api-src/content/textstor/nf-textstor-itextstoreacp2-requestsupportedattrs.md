---
UID: NF:textstor.ITextStoreACP2.RequestSupportedAttrs
title: ITextStoreACP2::RequestSupportedAttrs (textstor.h)
author: windows-sdk-content
description: Get the attributes that are supported in the document.
old-location: tsf\itextstoreacp2_requestsupportedattrs.htm
tech.root: TSF
ms.assetid: ce26c2ec-f808-4f59-bc54-b3681b97ad89
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextStoreACP2 interface [Text Services Framework],RequestSupportedAttrs method, ITextStoreACP2.RequestSupportedAttrs, ITextStoreACP2::RequestSupportedAttrs, RequestSupportedAttrs, RequestSupportedAttrs method [Text Services Framework], RequestSupportedAttrs method [Text Services Framework],ITextStoreACP2 interface, textstor/ITextStoreACP2::RequestSupportedAttrs, tsf.itextstoreacp2_requestsupportedattrs
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
 - ITextStoreACP2.RequestSupportedAttrs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStoreACP2::RequestSupportedAttrs


## -description


Get the attributes that are supported in the document.


## -parameters




### -param dwFlags [in]

Specifies whether a subsequent call to the <a href="https://msdn.microsoft.com/fff22304-626e-4ae6-ac8c-f4a62ee823c2">RetrieveRequestedAttrs</a> method will contain the supported attributes. If the <b>TS_ATTR_FIND_WANT_VALUE</b> flag is specified, the default attribute values will be those in the <a href="https://msdn.microsoft.com/9209ef60-6a1d-4aad-9f9f-775534116f37">TS_ATTRVAL</a> structure after the subsequent call to <b>RetrieveRequestedAttrs</b>. If any other flag is specified for this parameter, the method only verifies that the attribute is supported and that the <b>varValue</b> member of the <b>TS_ATTRVAL</b> structure is set to <b>VT_EMPTY</b>.


### -param cFilterAttrs [in]

Specifies the number of supported attributes to obtain.


### -param paFilterAttrs [in]

Pointer to the <a href="https://msdn.microsoft.com/5e375609-3d3c-4c12-ae05-dcaa70779162">TS_ATTRID</a> data type that specifies the attribute to verify. The method returns only the attributes specified by <b>TS_ATTRID</b>, even though other attributes can be supported.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate sufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c256f1c2-6b67-4417-8707-3490a2c5cb55">ITextStoreACP2</a>



<a href="https://msdn.microsoft.com/5e375609-3d3c-4c12-ae05-dcaa70779162">TS_ATTRID</a>



<a href="https://msdn.microsoft.com/9209ef60-6a1d-4aad-9f9f-775534116f37">TS_ATTRVAL</a>
 

 

