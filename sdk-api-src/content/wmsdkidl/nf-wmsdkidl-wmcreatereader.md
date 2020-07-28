---
UID: NF:wmsdkidl.WMCreateReader
title: WMCreateReader function (wmsdkidl.h)
description: The WMCreateReader function creates a reader object.
helpviewer_keywords: ["WMCreateReader","WMCreateReader function [windows Media Format]","wmformat.wmcreatereader","wmsdkidl/WMCreateReader"]
old-location: wmformat\wmcreatereader.htm
tech.root: wmformat
ms.assetid: f40d4b43-529d-4a78-80ec-4c339a91b28c
ms.date: 12/05/2018
ms.keywords: WMCreateReader, WMCreateReader function [windows Media Format], wmformat.wmcreatereader, wmsdkidl/WMCreateReader
f1_keywords:
- wmsdkidl/WMCreateReader
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wmvcore.dll
api_name:
- WMCreateReader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WMCreateReader function


## -description



The <b>WMCreateReader</b> function creates a reader object.




## -parameters




### -param pUnkCert [in]

This value must be set to <b>NULL</b>.


### -param dwRights [in]

<b>DWORD</b> indicating the desired operation. Set to one of the values from the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_rights">WMT_RIGHTS</a> enumeration type, indicating the operation that is performed on this file. If multiple operations are being performed, <i>dwRights</i> must consist of multiple values from <b>WMT_RIGHTS</b> combined by using the bitwise <b>OR</b> operator.


### -param ppReader [out]

Pointer to a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader</a> interface of the newly created reader object.


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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function is unable to allocate memory for the new object.

</td>
</tr>
</table>
 




## -remarks



After this object has been created, you can modify the rights that will be requested for the next file opened by calling <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty">IWMDRMReader::SetDRMProperty</a> with the <a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-rights">DRM_Rights</a> property. Note that when using this property, the rights are specified as strings, not as <b>DWORD</b> values.

The <i>dwRights</i> parameter may be set to 0 when reading non-DRM content. If <i>dwRights</i> is set to 0 and you open a protected file, you can access license related metadata, but you cannot read data from any streams in the file.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-attribute-list">DRM Attribute List</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-properties">DRM Properties</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/enabling-drm-support">Enabling DRM Support</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>
 

 

