---
UID: NF:wmsdkidl.IWMStreamConfig2.RemoveAllDataUnitExtensions
title: IWMStreamConfig2::RemoveAllDataUnitExtensions (wmsdkidl.h)
description: The RemoveAllDataUnitExtensions method removes all data unit extension systems that are associated with the stream.
helpviewer_keywords: ["IWMStreamConfig2 interface [windows Media Format]","RemoveAllDataUnitExtensions method","IWMStreamConfig2.RemoveAllDataUnitExtensions","IWMStreamConfig2::RemoveAllDataUnitExtensions","IWMStreamConfig2RemoveAllDataUnitExtensions","RemoveAllDataUnitExtensions","RemoveAllDataUnitExtensions method [windows Media Format]","RemoveAllDataUnitExtensions method [windows Media Format]","IWMStreamConfig2 interface","wmformat.iwmstreamconfig2_removealldataunitextensions","wmsdkidl/IWMStreamConfig2::RemoveAllDataUnitExtensions"]
old-location: wmformat\iwmstreamconfig2_removealldataunitextensions.htm
tech.root: wmformat
ms.assetid: 944c1b6c-1d1b-4a44-9b9e-d673c8d60306
ms.date: 4/26/2023
ms.keywords: IWMStreamConfig2 interface [windows Media Format],RemoveAllDataUnitExtensions method, IWMStreamConfig2.RemoveAllDataUnitExtensions, IWMStreamConfig2::RemoveAllDataUnitExtensions, IWMStreamConfig2RemoveAllDataUnitExtensions, RemoveAllDataUnitExtensions, RemoveAllDataUnitExtensions method [windows Media Format], RemoveAllDataUnitExtensions method [windows Media Format],IWMStreamConfig2 interface, wmformat.iwmstreamconfig2_removealldataunitextensions, wmsdkidl/IWMStreamConfig2::RemoveAllDataUnitExtensions
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
 - IWMStreamConfig2::RemoveAllDataUnitExtensions
 - wmsdkidl/IWMStreamConfig2::RemoveAllDataUnitExtensions
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
 - IWMStreamConfig2.RemoveAllDataUnitExtensions
---

# IWMStreamConfig2::RemoveAllDataUnitExtensions


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>RemoveAllDataUnitExtensions</b> method removes all data unit extension systems that are associated with the stream.



## -returns

The method always returns S_OK.

## -remarks

The changes will not take effect in the profile until you call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream">IWMProfile::ReconfigStream</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2">IWMStreamConfig2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension">IWMStreamConfig2::AddDataUnitExtension</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension">IWMStreamConfig2::GetDataUnitExtension</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount">IWMStreamConfig2::GetDataUnitExtensionCount</a>
