---
UID: NF:wmsdkidl.IWMStreamConfig.SetStreamNumber
title: IWMStreamConfig::SetStreamNumber (wmsdkidl.h)
description: The SetStreamNumber method specifies the stream number.
helpviewer_keywords: ["IWMStreamConfig interface [windows Media Format]","SetStreamNumber method","IWMStreamConfig.SetStreamNumber","IWMStreamConfig::SetStreamNumber","IWMStreamConfigSetStreamNumber","SetStreamNumber","SetStreamNumber method [windows Media Format]","SetStreamNumber method [windows Media Format]","IWMStreamConfig interface","wmformat.iwmstreamconfig_setstreamnumber","wmsdkidl/IWMStreamConfig::SetStreamNumber"]
old-location: wmformat\iwmstreamconfig_setstreamnumber.htm
tech.root: wmformat
ms.assetid: aea8b219-5b47-4176-ad96-d52646d96578
ms.date: 12/05/2018
ms.keywords: IWMStreamConfig interface [windows Media Format],SetStreamNumber method, IWMStreamConfig.SetStreamNumber, IWMStreamConfig::SetStreamNumber, IWMStreamConfigSetStreamNumber, SetStreamNumber, SetStreamNumber method [windows Media Format], SetStreamNumber method [windows Media Format],IWMStreamConfig interface, wmformat.iwmstreamconfig_setstreamnumber, wmsdkidl/IWMStreamConfig::SetStreamNumber
f1_keywords:
- wmsdkidl/IWMStreamConfig.SetStreamNumber
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
- IWMStreamConfig.SetStreamNumber
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMStreamConfig::SetStreamNumber


## -description



The <b>SetStreamNumber</b> method specifies the stream number.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number. Stream numbers must be in the range of 1 through 63.


## -returns



This method always returns S_OK.




## -remarks



The new value will not take effect in the profile until you call <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream">IWMProfile::ReconfigStream</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getstreamnumber">IWMStreamConfig::GetStreamNumber</a>
 

 

