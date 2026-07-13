---
UID: NF:wmsdkidl.IWMDRMReader.MonitorLicenseAcquisition
title: IWMDRMReader::MonitorLicenseAcquisition (wmsdkidl.h)
description: The MonitorLicenseAcquisition method, in nonsilent license acquisition, informs the application when a license has been successfully acquired.
helpviewer_keywords: ["IWMDRMReader interface [windows Media Format]","MonitorLicenseAcquisition method","IWMDRMReader.MonitorLicenseAcquisition","IWMDRMReader::MonitorLicenseAcquisition","IWMDRMReaderMonitorLicenseAcquisition","MonitorLicenseAcquisition","MonitorLicenseAcquisition method [windows Media Format]","MonitorLicenseAcquisition method [windows Media Format]","IWMDRMReader interface","wmformat.iwmdrmreader_monitorlicenseacquisition","wmsdkidl/IWMDRMReader::MonitorLicenseAcquisition"]
old-location: wmformat\iwmdrmreader_monitorlicenseacquisition.htm
tech.root: wmformat
ms.assetid: 0b15dce6-7591-479a-b28e-5006418a1c7b
ms.date: 4/26/2023
ms.keywords: IWMDRMReader interface [windows Media Format],MonitorLicenseAcquisition method, IWMDRMReader.MonitorLicenseAcquisition, IWMDRMReader::MonitorLicenseAcquisition, IWMDRMReaderMonitorLicenseAcquisition, MonitorLicenseAcquisition, MonitorLicenseAcquisition method [windows Media Format], MonitorLicenseAcquisition method [windows Media Format],IWMDRMReader interface, wmformat.iwmdrmreader_monitorlicenseacquisition, wmsdkidl/IWMDRMReader::MonitorLicenseAcquisition
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
 - IWMDRMReader::MonitorLicenseAcquisition
 - wmsdkidl/IWMDRMReader::MonitorLicenseAcquisition
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
 - IWMDRMReader.MonitorLicenseAcquisition
---

# IWMDRMReader::MonitorLicenseAcquisition


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>MonitorLicenseAcquisition</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>MonitorLicenseAcquisition</b> method, in nonsilent license acquisition, informs the application when a license has been successfully acquired.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method should be used whenever nonsilent license acquisition has been initiated for DRM version 7 content. It is an asynchronous call that returns immediately. This method creates a thread that periodically checks the local license store to determine when the requested license has been received. To cancel the attempt, call <b>CancelMonitorLicenseAcquisition</b>.

When the license acquisition is completed (whether successful or otherwise), the application is notified through a <b>WMT_LICENSE_ACQUIRE</b> event that is sent to the application's <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> method.

## -see-also

<a href="/windows/desktop/wmformat/handling-license-acquisition-events">Handling License Acquisition Events</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader">IWMDRMReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelmonitorlicenseacquisition">IWMDRMReader::CancelMonitorLicenseAcquisition</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a>
