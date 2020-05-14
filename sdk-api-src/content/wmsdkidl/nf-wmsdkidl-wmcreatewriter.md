---
UID: NF:wmsdkidl.WMCreateWriter
title: WMCreateWriter function (wmsdkidl.h)
description: The WMCreateWriter function creates a writer object.helpviewer_keywords: ["WMCreateWriter","WMCreateWriter function [windows Media Format]","wmformat.wmcreatewriter","wmsdkidl/WMCreateWriter"]
old-location: wmformat\wmcreatewriter.htm
tech.root: wmformat
ms.assetid: 26d42213-40a1-4e2c-805b-c0803ee015b4
ms.date: 12/05/2018
ms.keywords: WMCreateWriter, WMCreateWriter function [windows Media Format], wmformat.wmcreatewriter, wmsdkidl/WMCreateWriter
f1_keywords:
- wmsdkidl/WMCreateWriter
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
- WMCreateWriter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WMCreateWriter function


## -description



The <b>WMCreateWriter</b> function creates a writer object.




## -parameters




### -param pUnkCert [in]

Pointer to an <b>IUnknown</b> interface. This value is not used and should be set to <b>NULL</b>.


### -param ppWriter [out]

Pointer to a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter">IWMWriter</a> interface of the newly created writer object.


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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>
 

 

