---
UID: NF:mfidl.IMFSourceResolver.EndCreateObjectFromURL
title: IMFSourceResolver::EndCreateObjectFromURL (mfidl.h)
description: Completes an asynchronous request to create an object from a URL. (IMFSourceResolver.EndCreateObjectFromURL)
helpviewer_keywords: ["EndCreateObjectFromURL","EndCreateObjectFromURL method [Media Foundation]","EndCreateObjectFromURL method [Media Foundation]","IMFSourceResolver interface","IMFSourceResolver interface [Media Foundation]","EndCreateObjectFromURL method","IMFSourceResolver.EndCreateObjectFromURL","IMFSourceResolver::EndCreateObjectFromURL","af50a76d-b083-4815-bbff-820b21ff8d1b","mf.imfsourceresolver_endcreateobjectfromurl","mfidl/IMFSourceResolver::EndCreateObjectFromURL"]
old-location: mf\imfsourceresolver_endcreateobjectfromurl.htm
tech.root: mf
ms.assetid: af50a76d-b083-4815-bbff-820b21ff8d1b
ms.date: 12/05/2018
ms.keywords: EndCreateObjectFromURL, EndCreateObjectFromURL method [Media Foundation], EndCreateObjectFromURL method [Media Foundation],IMFSourceResolver interface, IMFSourceResolver interface [Media Foundation],EndCreateObjectFromURL method, IMFSourceResolver.EndCreateObjectFromURL, IMFSourceResolver::EndCreateObjectFromURL, af50a76d-b083-4815-bbff-820b21ff8d1b, mf.imfsourceresolver_endcreateobjectfromurl, mfidl/IMFSourceResolver::EndCreateObjectFromURL
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSourceResolver::EndCreateObjectFromURL
 - mfidl/IMFSourceResolver::EndCreateObjectFromURL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSourceResolver.EndCreateObjectFromURL
---

# IMFSourceResolver::EndCreateObjectFromURL


## -description

Completes an asynchronous request to create an object from a URL.

## -parameters

### -param pResult [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">Invoke</a> method.

### -param pObjectType [out]

Receives a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mf_object_type">MF_OBJECT_TYPE</a> enumeration, specifying the type of object that was created.

### -param ppObject [out]

Receives a pointer to the media source's <b>IUnknown</b> interface. The caller must release the interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The operation was canceled.
              

</td>
</tr>
</table>

## -remarks

Call this method from inside your application's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver">IMFSourceResolver</a>



<a href="/windows/desktop/medfound/source-resolver">Source Resolver</a>
