---
UID: NF:mfidl.MFCreateSimpleTypeHandler
title: MFCreateSimpleTypeHandler function (mfidl.h)
description: Creates a media-type handler that supports a single media type at a time.
helpviewer_keywords: ["441bd03d-b314-4f26-ad67-e6997e5edc9d","MFCreateSimpleTypeHandler","MFCreateSimpleTypeHandler function [Media Foundation]","mf.mfcreatesimpletypehandler","mfidl/MFCreateSimpleTypeHandler"]
old-location: mf\mfcreatesimpletypehandler.htm
tech.root: mf
ms.assetid: 441bd03d-b314-4f26-ad67-e6997e5edc9d
ms.date: 12/05/2018
ms.keywords: 441bd03d-b314-4f26-ad67-e6997e5edc9d, MFCreateSimpleTypeHandler, MFCreateSimpleTypeHandler function [Media Foundation], mf.mfcreatesimpletypehandler, mfidl/MFCreateSimpleTypeHandler
f1_keywords:
- mfidl/MFCreateSimpleTypeHandler
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- mf.dll
api_name:
- MFCreateSimpleTypeHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateSimpleTypeHandler function


## -description



Creates a media-type handler that supports a single media type at a time.




## -parameters




### -param ppHandler [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler">IMFMediaTypeHandler</a> interface of the media-type handler. The caller must release the interface.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>
 




## -remarks



The media-type handler created by this function supports one media type at a time. Set the media type by calling <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype">IMFMediaTypeHandler::SetCurrentMediaType</a>. After the type is set, <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported">IMFMediaTypeHandler::IsMediaTypeSupported</a> always checks against that type.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

