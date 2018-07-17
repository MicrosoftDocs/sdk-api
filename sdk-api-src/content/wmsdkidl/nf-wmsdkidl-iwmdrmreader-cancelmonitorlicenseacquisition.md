---
UID: NF:wmsdkidl.IWMDRMReader.CancelMonitorLicenseAcquisition
title: IWMDRMReader::CancelMonitorLicenseAcquisition
author: windows-sdk-content
description: The CancelMonitorLicenseAcquisition method cancels a current call to the MonitorLicenseAcquisition method.
old-location: wmformat\iwmdrmreader_cancelmonitorlicenseacquisition.htm
old-project: wmformat
ms.assetid: 9d33f727-9213-4744-bf65-42b971e3f7da
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CancelMonitorLicenseAcquisition, CancelMonitorLicenseAcquisition method [windows Media Format], CancelMonitorLicenseAcquisition method [windows Media Format],IWMDRMReader interface, IWMDRMReader interface [windows Media Format],CancelMonitorLicenseAcquisition method, IWMDRMReader.CancelMonitorLicenseAcquisition, IWMDRMReader::CancelMonitorLicenseAcquisition, IWMDRMReaderCancelMonitorLicenseAcquisition, wmformat.iwmdrmreader_cancelmonitorlicenseacquisition, wmsdkidl/IWMDRMReader::CancelMonitorLicenseAcquisition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WM_AETYPE
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
product: Windows
targetos: Windows
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDRMReader::CancelMonitorLicenseAcquisition


## -description


<p class="CCE_Message">[<b>CancelMonitorLicenseAcquisition</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>CancelMonitorLicenseAcquisition</b> method cancels a current call to the <a href="https://msdn.microsoft.com/0b15dce6-7591-479a-b28e-5006418a1c7b">MonitorLicenseAcquisition</a> method.




## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method terminates the thread that periodically checks the license store to determine when the most recently requested license has been obtained.




## -see-also




<a href="https://msdn.microsoft.com/bf4ff0f3-1f78-43c4-be4d-c74209176e58">IWMDRMReader Interface</a>
 

 

