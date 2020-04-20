---
UID: NF:wmsdkvalidate.WMValidateData
title: WMValidateData function (wmsdkvalidate.h)
description: The WMValidateData function verifies that data from the beginning of a file is consistent with the header section of a file type that is supported by the Windows Media Format SDK.helpviewer_keywords: ["WMValidateData","WMValidateData function [windows Media Format]","wmformat.wmvalidatedata","wmsdkvalidate/WMValidateData"]
old-location: wmformat\wmvalidatedata.htm
tech.root: wmformat
ms.assetid: 0bbe4ccc-a052-4bb9-ac6b-31d57ccf3bab
ms.date: 12/05/2018
ms.keywords: WMValidateData, WMValidateData function [windows Media Format], wmformat.wmvalidatedata, wmsdkvalidate/WMValidateData
f1_keywords:
- wmsdkvalidate/WMValidateData
dev_langs:
- c++
req.header: wmsdkvalidate.h
req.include-header: Wmsdkidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
- WMValidateData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WMValidateData function


## -description



The <b>WMValidateData</b> function verifies that data from the beginning of a file is consistent with the header section of a file type that is supported by the Windows Media Format SDK.



If you are writing an application that can handle many different file types, you can use this function to try to quickly determine whether the file can be read using the Windows Media Format SDK.


## -parameters




### -param pbData [in]

Pointer to a <b>BYTE</b> array containing the data buffer to validate. This data should be part of a file, starting at the beginning of the file, and continuing for the number of bytes specified in <i>pdwDataSize</i>.

You can set this parameter to <b>NULL</b> to retrieve the minimum number of bytes to pass.


### -param pdwDataSize [in, out]

Pointer to a <b>DWORD</b> containing the data size. If <i>pbData</i> is set to <b>NULL</b>, this value will be set to the minimum buffer size on return. The minimum buffer size is 512 bytes.


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
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The file cannot be handled by the objects of the Windows Media Format SDK.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pdwDataSize</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwDataSize</i> parameter points to a value that is smaller than the minimum data buffer required to validate the data.

</td>
</tr>
</table>
 




## -remarks



This function is typically used after a call to <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlextension">WMCheckURLExtension</a>. This is for efficiency, because <b>WMValidateData</b> requires that you read some of the data from the file, whereas <b>WMCheckURLExtension</b> only evaluates the file name extension.

It is possible for this function to identify a file as playable when it is not playable. However, if the function identifies a file as not playable, the file is certainly not playable.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/functions">Functions</a>
 

 

