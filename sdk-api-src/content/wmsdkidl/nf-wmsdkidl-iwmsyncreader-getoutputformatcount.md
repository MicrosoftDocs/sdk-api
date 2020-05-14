---
UID: NF:wmsdkidl.IWMSyncReader.GetOutputFormatCount
title: IWMSyncReader::GetOutputFormatCount (wmsdkidl.h)
description: The GetOutputFormatCount method is used to determine all possible format types supported by this output on the synchronous reader.helpviewer_keywords: ["GetOutputFormatCount","GetOutputFormatCount method [windows Media Format]","GetOutputFormatCount method [windows Media Format]","IWMSyncReader interface","IWMSyncReader interface [windows Media Format]","GetOutputFormatCount method","IWMSyncReader.GetOutputFormatCount","IWMSyncReader::GetOutputFormatCount","IWMSyncReaderGetOutputFormatCount","wmformat.iwmsyncreader_getoutputformatcount","wmsdkidl/IWMSyncReader::GetOutputFormatCount"]
old-location: wmformat\iwmsyncreader_getoutputformatcount.htm
tech.root: wmformat
ms.assetid: 66f66784-791b-4f1b-8ba2-300a4521ce03
ms.date: 12/05/2018
ms.keywords: GetOutputFormatCount, GetOutputFormatCount method [windows Media Format], GetOutputFormatCount method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetOutputFormatCount method, IWMSyncReader.GetOutputFormatCount, IWMSyncReader::GetOutputFormatCount, IWMSyncReaderGetOutputFormatCount, wmformat.iwmsyncreader_getoutputformatcount, wmsdkidl/IWMSyncReader::GetOutputFormatCount
f1_keywords:
- wmsdkidl/IWMSyncReader.GetOutputFormatCount
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wmvcore.lib
- Wmvcore.dll
- WMStubDRM.lib
- WMStubDRM.dll
api_name:
- IWMSyncReader.GetOutputFormatCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMSyncReader::GetOutputFormatCount


## -description



The <b>GetOutputFormatCount</b> method is used to determine all possible format types supported by this output on the synchronous reader.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number for which you want to determine the number of supported formats.


### -param pcFormats [out]

Pointer to a <b>DWORD</b> that receives the number of supported formats.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pcFormats</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
There is no file loaded in the synchronous reader.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat">IWMSyncReader::GetOutputFormat</a>
 

 

