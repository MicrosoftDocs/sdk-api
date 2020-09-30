---
UID: NF:wmsdkidl.IWMDRMReader.CancelIndividualization
title: IWMDRMReader::CancelIndividualization (wmsdkidl.h)
description: The CancelIndividualization method cancels a current call to the Individualize method.
helpviewer_keywords: ["CancelIndividualization","CancelIndividualization method [windows Media Format]","CancelIndividualization method [windows Media Format]","IWMDRMReader interface","IWMDRMReader interface [windows Media Format]","CancelIndividualization method","IWMDRMReader.CancelIndividualization","IWMDRMReader::CancelIndividualization","IWMDRMReaderCancelIndividualization","wmformat.iwmdrmreader_cancelindividualization","wmsdkidl/IWMDRMReader::CancelIndividualization"]
old-location: wmformat\iwmdrmreader_cancelindividualization.htm
tech.root: wmformat
ms.assetid: 837d6fee-d5ba-49d8-ac69-e8ff010a787d
ms.date: 12/05/2018
ms.keywords: CancelIndividualization, CancelIndividualization method [windows Media Format], CancelIndividualization method [windows Media Format],IWMDRMReader interface, IWMDRMReader interface [windows Media Format],CancelIndividualization method, IWMDRMReader.CancelIndividualization, IWMDRMReader::CancelIndividualization, IWMDRMReaderCancelIndividualization, wmformat.iwmdrmreader_cancelindividualization, wmsdkidl/IWMDRMReader::CancelIndividualization
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
 - IWMDRMReader::CancelIndividualization
 - wmsdkidl/IWMDRMReader::CancelIndividualization
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
 - IWMDRMReader.CancelIndividualization
---

# IWMDRMReader::CancelIndividualization


## -description

<p class="CCE_Message">[<b>CancelIndividualization</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>CancelIndividualization</b> method cancels a current call to the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize">Individualize</a> method.

## -parameters

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader">IWMDRMReader Interface</a>