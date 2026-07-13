---
UID: NF:wmsdkidl.IWMDRMReader.SetDRMProperty
title: IWMDRMReader::SetDRMProperty (wmsdkidl.h)
description: The SetDRMProperty method on the reader object is used to set a DRM property, such as the DRM_Rights property.
helpviewer_keywords: ["IWMDRMReader interface [windows Media Format]","SetDRMProperty method","IWMDRMReader.SetDRMProperty","IWMDRMReader::SetDRMProperty","IWMDRMReaderSetDRMProperty","SetDRMProperty","SetDRMProperty method [windows Media Format]","SetDRMProperty method [windows Media Format]","IWMDRMReader interface","wmformat.iwmdrmreader_setdrmproperty","wmsdkidl/IWMDRMReader::SetDRMProperty"]
old-location: wmformat\iwmdrmreader_setdrmproperty.htm
tech.root: wmformat
ms.assetid: 52f606c2-a746-488f-bbf7-0d0e54b89bf9
ms.date: 4/26/2023
ms.keywords: IWMDRMReader interface [windows Media Format],SetDRMProperty method, IWMDRMReader.SetDRMProperty, IWMDRMReader::SetDRMProperty, IWMDRMReaderSetDRMProperty, SetDRMProperty, SetDRMProperty method [windows Media Format], SetDRMProperty method [windows Media Format],IWMDRMReader interface, wmformat.iwmdrmreader_setdrmproperty, wmsdkidl/IWMDRMReader::SetDRMProperty
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
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDRMReader::SetDRMProperty
 - wmsdkidl/IWMDRMReader::SetDRMProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMDRMReader.SetDRMProperty
---

# IWMDRMReader::SetDRMProperty


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>SetDRMProperty</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>SetDRMProperty</b> method on the reader object is used to set a DRM property, such as the <a href="/windows/desktop/wmformat/drm-rights">DRM_Rights</a> property.

## -parameters

### -param pwstrName [in]

Specifies the name of the property to set.

### -param dwType [in]

One member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a> enumeration type. The only supported value for this method is <b>WMT_TYPE_STRING</b>.

### -param pValue [in]

Pointer to a byte array containing the attribute value.

### -param cbLength [in]

Size of <i>pValue</i>, in bytes.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/wmformat/drm-attribute-list">DRM Attribute List</a>



<a href="/windows/desktop/wmformat/drm-properties">DRM Properties</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader">IWMDRMReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty">IWMDRMReader::GetDRMProperty</a>



<a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a>