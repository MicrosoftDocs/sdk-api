---
UID: NF:wmsdkidl.IWMReaderAdvanced2.GetSaveAsProgress
title: IWMReaderAdvanced2::GetSaveAsProgress (wmsdkidl.h)
description: The GetSaveAsProgress method retrieves the percentage of data that has been saved.
helpviewer_keywords: ["GetSaveAsProgress","GetSaveAsProgress method [windows Media Format]","GetSaveAsProgress method [windows Media Format]","IWMReaderAdvanced2 interface","IWMReaderAdvanced2 interface [windows Media Format]","GetSaveAsProgress method","IWMReaderAdvanced2.GetSaveAsProgress","IWMReaderAdvanced2::GetSaveAsProgress","IWMReaderAdvanced2GetSaveAsProgress","wmformat.iwmreaderadvanced2_getsaveasprogress","wmsdkidl/IWMReaderAdvanced2::GetSaveAsProgress"]
old-location: wmformat\iwmreaderadvanced2_getsaveasprogress.htm
tech.root: wmformat
ms.assetid: 0317f010-4b7f-4f79-9460-ba6b1e904ffa
ms.date: 12/05/2018
ms.keywords: GetSaveAsProgress, GetSaveAsProgress method [windows Media Format], GetSaveAsProgress method [windows Media Format],IWMReaderAdvanced2 interface, IWMReaderAdvanced2 interface [windows Media Format],GetSaveAsProgress method, IWMReaderAdvanced2.GetSaveAsProgress, IWMReaderAdvanced2::GetSaveAsProgress, IWMReaderAdvanced2GetSaveAsProgress, wmformat.iwmreaderadvanced2_getsaveasprogress, wmsdkidl/IWMReaderAdvanced2::GetSaveAsProgress
f1_keywords:
- wmsdkidl/IWMReaderAdvanced2.GetSaveAsProgress
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
- IWMReaderAdvanced2.GetSaveAsProgress
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced2::GetSaveAsProgress


## -description



The <b>GetSaveAsProgress</b> method retrieves the percentage of data that has been saved.




## -parameters




### -param pdwPercent [out]

Pointer to a <b>DWORD</b> containing the percentage of data that has been saved.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method must only be called after <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas">IWMReaderAdvanced2::SaveFileAs</a> has been called.

When saving a file, the operation can take some time. This call must be made between the events WMT_SAVEAS_START and WMT_SAVEAS_STOP. If it is called before WMT_SAVEAS_START, or there is an error, this method returns zero. It returns 100 following a successful WMT_SAVEAS_STOP event.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>
 

 

