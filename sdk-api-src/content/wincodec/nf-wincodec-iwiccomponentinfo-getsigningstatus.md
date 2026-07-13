---
UID: NF:wincodec.IWICComponentInfo.GetSigningStatus
title: IWICComponentInfo::GetSigningStatus (wincodec.h)
description: Retrieves the signing status of the component.
helpviewer_keywords: ["GetSigningStatus","GetSigningStatus method [Windows Imaging Component]","GetSigningStatus method [Windows Imaging Component]","IWICComponentInfo interface","IWICComponentInfo interface [Windows Imaging Component]","GetSigningStatus method","IWICComponentInfo.GetSigningStatus","IWICComponentInfo::GetSigningStatus","_wic_codec_iwiccomponentinfo_getsigningstatus","wic._wic_codec_iwiccomponentinfo_getsigningstatus","wincodec/IWICComponentInfo::GetSigningStatus"]
old-location: wic\_wic_codec_iwiccomponentinfo_getsigningstatus.htm
tech.root: wic
ms.assetid: a6d13240-3750-4450-8069-7e05dd89f2ab
ms.date: 12/05/2018
ms.keywords: GetSigningStatus, GetSigningStatus method [Windows Imaging Component], GetSigningStatus method [Windows Imaging Component],IWICComponentInfo interface, IWICComponentInfo interface [Windows Imaging Component],GetSigningStatus method, IWICComponentInfo.GetSigningStatus, IWICComponentInfo::GetSigningStatus, _wic_codec_iwiccomponentinfo_getsigningstatus, wic._wic_codec_iwiccomponentinfo_getsigningstatus, wincodec/IWICComponentInfo::GetSigningStatus
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICComponentInfo::GetSigningStatus
 - wincodec/IWICComponentInfo::GetSigningStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICComponentInfo.GetSigningStatus
---

# IWICComponentInfo::GetSigningStatus


## -description

Retrieves the signing status of the component.

## -parameters

### -param pStatus [out]

Type: <b>DWORD*</b>

A pointer that receives the <a href="/windows/desktop/api/wincodec/ne-wincodec-wiccomponentsigning">WICComponentSigning</a> status of the component.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Signing is unused by WIC. Therefore, all components WICComponentSigned.

This function can be used to determine whether a component has no binary component or has been added to the disabled components list in the registry.