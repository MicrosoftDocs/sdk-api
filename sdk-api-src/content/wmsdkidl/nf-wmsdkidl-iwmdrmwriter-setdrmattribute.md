---
UID: NF:wmsdkidl.IWMDRMWriter.SetDRMAttribute
title: IWMDRMWriter::SetDRMAttribute (wmsdkidl.h)
description: The SetDRMAttribute method sets DRM-header attributes as well as other DRM run-time properties.
helpviewer_keywords: ["IWMDRMWriter interface [windows Media Format]","SetDRMAttribute method","IWMDRMWriter.SetDRMAttribute","IWMDRMWriter::SetDRMAttribute","IWMDRMWriterSetDRMAttribute","SetDRMAttribute","SetDRMAttribute method [windows Media Format]","SetDRMAttribute method [windows Media Format]","IWMDRMWriter interface","wmformat.iwmdrmwriter_setdrmattribute","wmsdkidl/IWMDRMWriter::SetDRMAttribute"]
old-location: wmformat\iwmdrmwriter_setdrmattribute.htm
tech.root: wmformat
ms.assetid: f54bba2a-872e-4ed1-b2c6-3e6b85a48df6
ms.date: 4/26/2023
ms.keywords: IWMDRMWriter interface [windows Media Format],SetDRMAttribute method, IWMDRMWriter.SetDRMAttribute, IWMDRMWriter::SetDRMAttribute, IWMDRMWriterSetDRMAttribute, SetDRMAttribute, SetDRMAttribute method [windows Media Format], SetDRMAttribute method [windows Media Format],IWMDRMWriter interface, wmformat.iwmdrmwriter_setdrmattribute, wmsdkidl/IWMDRMWriter::SetDRMAttribute
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
 - IWMDRMWriter::SetDRMAttribute
 - wmsdkidl/IWMDRMWriter::SetDRMAttribute
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
 - IWMDRMWriter.SetDRMAttribute
---

# IWMDRMWriter::SetDRMAttribute


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>SetDRMAttribute</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>SetDRMAttribute</b> method sets DRM-header attributes as well as other DRM run-time properties.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number to which the attribute applies.

### -param pszName [in]

Pointer to a null-terminated string containing the attribute name. See Remarks for supported attributes.

### -param Type [in]

A value from the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a> enumeration type specifying the data type of the attribute data.

### -param pValue [in]

Pointer to an array of bytes containing the attribute data.

### -param cbLength [in]

The size, in bytes, of the attribute data pointed to by <i>pValue</i>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method is somewhat misnamed because it is used to set not only writable DRM file attributes (See <a href="/windows/desktop/wmformat/drm-attribute-list">DRM Attribute List</a>), but also certain DRM properties that are used by the DRM run-time components but are not written to the DRM header in the file. (See <a href="/windows/desktop/wmformat/drm-properties">DRM Properties</a>.)

The properties <b>Use_Advanced_DRM</b> and <b>Use_DRM</b> may be specified before a profile is set. No other properties can be set before a profile is set. The following code snippet shows how to call this function, using the <a href="/windows/desktop/wmformat/drm-contentid">DRM_ContentID</a> property as an example. Assume that <i>pDRMWriter</i> is a <b>IWMDRMWriter</b> interface pointer, and <i>wszContentID</i> is an array of type <b>WCHAR</b>.


```cpp

hr = pDRMWriter->SetDRMAttribute( 0, g_wszWMDRM_ContentID, 
        WMT_TYPE_STRING, (BYTE *)wszContentID, 
        ( wcslen( wszContentID ) + 1 ) * sizeof( WCHAR ) );

```

## -see-also

<a href="/windows/desktop/wmformat/drm-attribute-list">DRM Attribute List</a>



<a href="/windows/desktop/wmformat/drm-properties">DRM Properties</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter">IWMDRMWriter Interface</a>