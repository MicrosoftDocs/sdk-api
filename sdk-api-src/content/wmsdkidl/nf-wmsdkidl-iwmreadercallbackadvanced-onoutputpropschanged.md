---
UID: NF:wmsdkidl.IWMReaderCallbackAdvanced.OnOutputPropsChanged
title: IWMReaderCallbackAdvanced::OnOutputPropsChanged (wmsdkidl.h)
description: The OnOutputPropsChanged method indicates that the media properties for the specified output have changed. This change occurs as a result of a call to the IWMReader::SetOutputProps method.
helpviewer_keywords: ["IWMReaderCallbackAdvanced interface [windows Media Format]","OnOutputPropsChanged method","IWMReaderCallbackAdvanced.OnOutputPropsChanged","IWMReaderCallbackAdvanced::OnOutputPropsChanged","IWMReaderCallbackAdvancedOnOutputPropsChanged","OnOutputPropsChanged","OnOutputPropsChanged method [windows Media Format]","OnOutputPropsChanged method [windows Media Format]","IWMReaderCallbackAdvanced interface","wmformat.iwmreadercallbackadvanced_onoutputpropschanged","wmsdkidl/IWMReaderCallbackAdvanced::OnOutputPropsChanged"]
old-location: wmformat\iwmreadercallbackadvanced_onoutputpropschanged.htm
tech.root: wmformat
ms.assetid: 5e8193c4-5fc7-4b19-9f6e-6873ebe5156a
ms.date: 12/05/2018
ms.keywords: IWMReaderCallbackAdvanced interface [windows Media Format],OnOutputPropsChanged method, IWMReaderCallbackAdvanced.OnOutputPropsChanged, IWMReaderCallbackAdvanced::OnOutputPropsChanged, IWMReaderCallbackAdvancedOnOutputPropsChanged, OnOutputPropsChanged, OnOutputPropsChanged method [windows Media Format], OnOutputPropsChanged method [windows Media Format],IWMReaderCallbackAdvanced interface, wmformat.iwmreadercallbackadvanced_onoutputpropschanged, wmsdkidl/IWMReaderCallbackAdvanced::OnOutputPropsChanged
f1_keywords:
- wmsdkidl/IWMReaderCallbackAdvanced.OnOutputPropsChanged
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wmsdkidl.h
api_name:
- IWMReaderCallbackAdvanced.OnOutputPropsChanged
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderCallbackAdvanced::OnOutputPropsChanged


## -description



The <b>OnOutputPropsChanged</b> method indicates that the media properties for the specified output have changed. This change occurs as a result of a call to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops">IWMReader::SetOutputProps</a> method.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.


### -param pMediaType [in]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type">WM_MEDIA_TYPE</a> structure.


### -param pvContext [in]

Generic pointer, for use by the application. This pointer is the context pointer given to the <b>IWMReader::Start</b> method.


## -returns



To use this method, you must implement it in your application. You can return whatever <b>HRESULT</b> error codes are appropriate to your implementation. For more information about the <b>HRESULT</b> error codes included for use by the Windows Media Format SDK, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/error-codes">Error Codes</a>.




## -remarks



This method is called by the reader if the caller gets an asynchronous result from the <b>SetOutputProps</b> method call. The next sample received for this output has these properties. After a call to <b>SetOutputProps</b> and before <b>OnOutputPropsChanged</b> is called, the contents of the media type are undefined.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced">IWMReaderCallbackAdvanced Interface</a>
 

 

