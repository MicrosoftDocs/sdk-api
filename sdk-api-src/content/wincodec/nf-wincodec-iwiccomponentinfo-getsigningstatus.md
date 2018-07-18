---
UID: NF:wincodec.IWICComponentInfo.GetSigningStatus
title: IWICComponentInfo::GetSigningStatus
author: windows-sdk-content
description: Retrieves the signing status of the component.
old-location: wic\_wic_codec_iwiccomponentinfo_getsigningstatus.htm
old-project: wic
ms.assetid: a6d13240-3750-4450-8069-7e05dd89f2ab
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetSigningStatus, GetSigningStatus method [Windows Imaging Component], GetSigningStatus method [Windows Imaging Component],IWICComponentInfo interface, IWICComponentInfo interface [Windows Imaging Component],GetSigningStatus method, IWICComponentInfo.GetSigningStatus, IWICComponentInfo::GetSigningStatus, _wic_codec_iwiccomponentinfo_getsigningstatus, wic._wic_codec_iwiccomponentinfo_getsigningstatus, wincodec/IWICComponentInfo::GetSigningStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WICTiffCompressionOption
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
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICComponentInfo::GetSigningStatus


## -description


Retrieves the signing status of the component.


## -parameters




### -param pStatus [out]

Type: <b>DWORD*</b>

A pointer that receives the <a href="https://msdn.microsoft.com/64f3de6d-15da-4cc8-ad74-57759bcd4d07">WICComponentSigning</a> status of the component.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Signing is unused by WIC. Therefore, all components WICComponentSigned.

This function can be used to determine whether a component has no binary component or has been added to the disabled components list in the registry.



