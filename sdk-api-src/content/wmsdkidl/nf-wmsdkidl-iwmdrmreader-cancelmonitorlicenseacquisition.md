---
UID: NF:wmsdkidl.IWMDRMReader.CancelMonitorLicenseAcquisition
title: IWMDRMReader::CancelMonitorLicenseAcquisition (wmsdkidl.h)
description: The CancelMonitorLicenseAcquisition method cancels a current call to the MonitorLicenseAcquisition method.
helpviewer_keywords: ["CancelMonitorLicenseAcquisition","CancelMonitorLicenseAcquisition method [windows Media Format]","CancelMonitorLicenseAcquisition method [windows Media Format]","IWMDRMReader interface","IWMDRMReader interface [windows Media Format]","CancelMonitorLicenseAcquisition method","IWMDRMReader.CancelMonitorLicenseAcquisition","IWMDRMReader::CancelMonitorLicenseAcquisition","IWMDRMReaderCancelMonitorLicenseAcquisition","wmformat.iwmdrmreader_cancelmonitorlicenseacquisition","wmsdkidl/IWMDRMReader::CancelMonitorLicenseAcquisition"]
old-location: wmformat\iwmdrmreader_cancelmonitorlicenseacquisition.htm
tech.root: wmformat
ms.assetid: 9d33f727-9213-4744-bf65-42b971e3f7da
ms.date: 4/26/2023
ms.keywords: CancelMonitorLicenseAcquisition, CancelMonitorLicenseAcquisition method [windows Media Format], CancelMonitorLicenseAcquisition method [windows Media Format],IWMDRMReader interface, IWMDRMReader interface [windows Media Format],CancelMonitorLicenseAcquisition method, IWMDRMReader.CancelMonitorLicenseAcquisition, IWMDRMReader::CancelMonitorLicenseAcquisition, IWMDRMReaderCancelMonitorLicenseAcquisition, wmformat.iwmdrmreader_cancelmonitorlicenseacquisition, wmsdkidl/IWMDRMReader::CancelMonitorLicenseAcquisition
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
 - IWMDRMReader::CancelMonitorLicenseAcquisition
 - wmsdkidl/IWMDRMReader::CancelMonitorLicenseAcquisition
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
 - IWMDRMReader.CancelMonitorLicenseAcquisition
---

# IWMDRMReader::CancelMonitorLicenseAcquisition


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>CancelMonitorLicenseAcquisition</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>CancelMonitorLicenseAcquisition</b> method cancels a current call to the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition">MonitorLicenseAcquisition</a> method.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method terminates the thread that periodically checks the license store to determine when the most recently requested license has been obtained.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader">IWMDRMReader Interface</a>
