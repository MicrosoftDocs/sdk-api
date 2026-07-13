---
UID: NF:wmsdkidl.IWMSyncReader.GetStreamNumberForOutput
title: IWMSyncReader::GetStreamNumberForOutput (wmsdkidl.h)
description: The GetStreamNumberForOutput method retrieves the stream number that corresponds with the specified output.
helpviewer_keywords: ["GetStreamNumberForOutput","GetStreamNumberForOutput method [windows Media Format]","GetStreamNumberForOutput method [windows Media Format]","IWMSyncReader interface","IWMSyncReader interface [windows Media Format]","GetStreamNumberForOutput method","IWMSyncReader.GetStreamNumberForOutput","IWMSyncReader::GetStreamNumberForOutput","IWMSyncReaderGetStreamNumberForOutput","wmformat.iwmsyncreader_getstreamnumberforoutput","wmsdkidl/IWMSyncReader::GetStreamNumberForOutput"]
old-location: wmformat\iwmsyncreader_getstreamnumberforoutput.htm
tech.root: wmformat
ms.assetid: 85543b80-78dd-4dc6-8885-c6a53f910165
ms.date: 4/26/2023
ms.keywords: GetStreamNumberForOutput, GetStreamNumberForOutput method [windows Media Format], GetStreamNumberForOutput method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetStreamNumberForOutput method, IWMSyncReader.GetStreamNumberForOutput, IWMSyncReader::GetStreamNumberForOutput, IWMSyncReaderGetStreamNumberForOutput, wmformat.iwmsyncreader_getstreamnumberforoutput, wmsdkidl/IWMSyncReader::GetStreamNumberForOutput
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMSyncReader::GetStreamNumberForOutput
 - wmsdkidl/IWMSyncReader::GetStreamNumberForOutput
dev_langs:
 - c++
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
 - IWMSyncReader.GetStreamNumberForOutput
---

# IWMSyncReader::GetStreamNumberForOutput


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetStreamNumberForOutput</b> method retrieves the stream number that corresponds with the specified output.

## -parameters

### -param dwOutputNum [in]

<b>DWORD</b> value specifying the output number for which you want to retrieve a stream number.

### -param pwStreamNum [out]

Pointer to a <b>WORD</b> value that receives the stream number that corresponds to the output specified by <i>dwOutput</i>.

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
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
<i>dwOutput</i> specifies an invalid output number.

</td>
</tr>
</table>

## -remarks

In the case of outputs that equate to mutual exclusions, only the active stream number is retrieved. If you need to get all of the stream numbers associated with such an output, you must access the profile information for the file.

## -see-also

<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>