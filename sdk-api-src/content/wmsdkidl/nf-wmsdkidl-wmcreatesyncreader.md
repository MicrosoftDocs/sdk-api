---
UID: NF:wmsdkidl.WMCreateSyncReader
title: WMCreateSyncReader function (wmsdkidl.h)
description: The WMCreateSyncReader function creates a synchronous reader object.
helpviewer_keywords: ["WMCreateSyncReader","WMCreateSyncReader function [windows Media Format]","wmformat.wmcreatesyncreader","wmsdkidl/WMCreateSyncReader"]
old-location: wmformat\wmcreatesyncreader.htm
tech.root: wmformat
ms.assetid: 77cb65cc-9785-4af4-9b92-245c17e5ab82
ms.date: 4/26/2023
ms.keywords: WMCreateSyncReader, WMCreateSyncReader function [windows Media Format], wmformat.wmcreatesyncreader, wmsdkidl/WMCreateSyncReader
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
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMCreateSyncReader
 - wmsdkidl/WMCreateSyncReader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-mm-wmvcore-l1-1-0.dll
 - Wmvcore.dll
api_name:
 - WMCreateSyncReader
---

# WMCreateSyncReader function


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMCreateSyncReader</b> function creates a synchronous reader object.

## -parameters

### -param pUnkCert [in]

Pointer to an <b>IUnknown</b> interface. This value must be set to <b>NULL</b>.

### -param dwRights [in]

<b>DWORD</b> specifying the desired operation. When playing back non-DRM content, or for an application that does not have DRM rights, this value can be set to zero. Otherwise, this value must be one of the values from the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_rights">WMT_RIGHTS</a> enumeration type, indicating the operation that is performed on this file. If multiple operations are being performed, <b>dwRights</b> must consist of multiple values from <b>WMT_RIGHTS</b> combined by using the bitwise <b>OR</b> operator.

### -param ppSyncReader [out]

Pointer to a pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader</a> interface of the newly created synchronous reader object.

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

<a href="/windows/desktop/wmformat/functions">Functions</a>



<a href="/windows/desktop/wmformat/synchronous-reader-object">Synchronous Reader Object</a>