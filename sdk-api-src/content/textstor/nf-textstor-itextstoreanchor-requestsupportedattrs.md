---
UID: NF:textstor.ITextStoreAnchor.RequestSupportedAttrs
title: ITextStoreAnchor::RequestSupportedAttrs
author: windows-sdk-content
description: ITextStoreAnchor::RequestSupportedAttrs method
old-location: tsf\itextstoreanchor_requestsupportedattrs.htm
tech.root: TSF
ms.assetid: ab81d79d-e991-4c2d-9fb7-95393e002828
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],RequestSupportedAttrs method, ITextStoreAnchor.RequestSupportedAttrs, ITextStoreAnchor::RequestSupportedAttrs, RequestSupportedAttrs, RequestSupportedAttrs method [Text Services Framework], RequestSupportedAttrs method [Text Services Framework],ITextStoreAnchor interface, textstor/ITextStoreAnchor::RequestSupportedAttrs, tsf.itextstoreanchor_requestsupportedattrs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
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
 - ITextStoreAnchor.RequestSupportedAttrs
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
- apiref
: 
- COM
: 
- textstor.h
: 
- ITextStoreAnchor.RequestSupportedAttrs
: 
---

# ITextStoreAnchor::RequestSupportedAttrs


## -description




## -parameters




### -param dwFlags [in]

Specifies whether a subsequent call to the <b>ITextStoreAnchor::RetrieveRequestedAttrs</b> method will contain the supported attributes. If the TS_ATTR_FIND_WANT_VALUE flag is specified, the default attribute values will be those in the <a href="https://msdn.microsoft.com/9209ef60-6a1d-4aad-9f9f-775534116f37">TS_ATTRVAL</a> structure after the subsequent call to <b>ITextStoreAnchor::RetrieveRequestedAttrs</b>. If any other flag is specified for this parameter, the method only verifies that the attribute is supported and that the <b>varValue</b> member of the <b>TS_ATTRVAL</b> structure is set to VT_EMPTY.


### -param cFilterAttrs [in]

Specifies the number of supported attributes to obtain.


### -param paFilterAttrs [in]

Pointer to the <a href="https://msdn.microsoft.com/5e375609-3d3c-4c12-ae05-dcaa70779162">TS_ATTRID</a> data type that specifies the attribute to verify. The method returns only the attributes specified by <b>TS_ATTRID</b>, even though other attributes might be supported.


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




<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a>



<a href="https://msdn.microsoft.com/36847680-bcf2-4db5-a587-90518f60cf5b">ITextStoreAnchor::RetrieveRequestedAttrs
      </a>



<a href="https://msdn.microsoft.com/5e375609-3d3c-4c12-ae05-dcaa70779162">TS_ATTRID
      </a>



<a href="https://msdn.microsoft.com/9209ef60-6a1d-4aad-9f9f-775534116f37">TS_ATTRVAL
      </a>
 

 

