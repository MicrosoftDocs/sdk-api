---
UID: NF:textstor.ITextStoreACP.RequestSupportedAttrs
title: ITextStoreACP::RequestSupportedAttrs (textstor.h)
author: windows-sdk-content
description: Get the attributes that are supported in the document.
old-location: tsf\itextstoreacp_requestsupportedattrs.htm
tech.root: TSF
ms.assetid: 243cd002-c882-4ce9-b528-1a2229c46f4a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextStoreACP interface [Text Services Framework],RequestSupportedAttrs method, ITextStoreACP.RequestSupportedAttrs, ITextStoreACP::RequestSupportedAttrs, RequestSupportedAttrs, RequestSupportedAttrs method [Text Services Framework], RequestSupportedAttrs method [Text Services Framework],ITextStoreACP interface, _tsf_itextstoreacp_requestsupportedattrs_ref, textstor/ITextStoreACP::RequestSupportedAttrs, tsf.itextstoreacp_requestsupportedattrs
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ITextStoreACP.RequestSupportedAttrs
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreACP::RequestSupportedAttrs


## -description


Get the attributes that are supported in the document.


## -parameters




### -param dwFlags [in]

Specifies whether a subsequent call to the <a href="https://msdn.microsoft.com/36847680-bcf2-4db5-a587-90518f60cf5b">ITextStoreAnchor::RetrieveRequestedAttrs</a> method will contain the supported attributes. If the TS_ATTR_FIND_WANT_VALUE flag is specified, the default attribute values will be those in the <a href="https://msdn.microsoft.com/9209ef60-6a1d-4aad-9f9f-775534116f37">TS_ATTRVAL</a> structure after the subsequent call to <b>ITextStoreAnchor::RetrieveRequestedAttrs</b>. If any other flag is specified for this parameter, the method only verifies that the attribute is supported and that the <b>varValue</b> member of the <b>TS_ATTRVAL</b> structure is set to VT_EMPTY.


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




<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a>



<a href="https://msdn.microsoft.com/6cd34ca5-6561-4161-beac-98248f0415f6">ITextStoreACP::RetrieveRequestededAttrs
      </a>



<a href="https://msdn.microsoft.com/5e375609-3d3c-4c12-ae05-dcaa70779162">TS_ATTRID
      </a>



<a href="https://msdn.microsoft.com/9209ef60-6a1d-4aad-9f9f-775534116f37">TS_ATTRVAL
      </a>
 

 

