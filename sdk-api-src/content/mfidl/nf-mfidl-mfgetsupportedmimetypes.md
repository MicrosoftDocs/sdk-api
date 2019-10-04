---
UID: NF:mfidl.MFGetSupportedMimeTypes
title: MFGetSupportedMimeTypes function (mfidl.h)
author: windows-sdk-content
description: Retrieves the MIME types that are registered for the source resolver.
old-location: mf\mfgetsupportedmimetypes.htm
tech.root: medfound
ms.assetid: 7e7b0e6e-98eb-4fb1-8577-e73eb9d62623
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 7e7b0e6e-98eb-4fb1-8577-e73eb9d62623, MFGetSupportedMimeTypes, MFGetSupportedMimeTypes function [Media Foundation], mf.mfgetsupportedmimetypes, mfidl/MFGetSupportedMimeTypes
ms.topic: function
f1_keywords: 
 - "mfidl/MFGetSupportedMimeTypes"
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
 - MFGetSupportedMimeTypes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFGetSupportedMimeTypes function


## -description



Retrieves the MIME types that are registered for the source resolver.




## -parameters




### -param pPropVarMimeTypeArray [out]

Pointer to a <b>PROPVARIANT</b> that receives the MIME types. Before calling this method, call <b>PropVariantInit</b> to initialize the <b>PROPVARIANT</b>. If the method succeeds, the <b>PROPVARIANT</b> contains an array of wide-character strings. The <b>PROPVARIANT</b> data type is VT_VECTOR | VT_LPWSTR. The caller must release the <b>PROPVARIANT</b> by calling <b>PropVariantClear</b>.


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
The function succeeded.
              

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

