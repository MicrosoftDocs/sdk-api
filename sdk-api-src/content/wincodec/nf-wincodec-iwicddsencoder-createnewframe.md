---
UID: NF:wincodec.IWICDdsEncoder.CreateNewFrame
title: IWICDdsEncoder::CreateNewFrame
author: windows-sdk-content
description: Creates a new frame to encode.
old-location: wic\iwicddsencoder_createnewframe.htm
tech.root: wic
ms.assetid: 14195781-DA71-400A-B4A7-F336A0B5429B
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateNewFrame, CreateNewFrame method [Windows Imaging Component], CreateNewFrame method [Windows Imaging Component],IWICDdsEncoder interface, IWICDdsEncoder interface [Windows Imaging Component],CreateNewFrame method, IWICDdsEncoder.CreateNewFrame, IWICDdsEncoder::CreateNewFrame, wic.iwicddsencoder_createnewframe, wincodec/IWICDdsEncoder::CreateNewFrame
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICDdsEncoder.CreateNewFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICDdsEncoder::CreateNewFrame


## -description


Creates a new frame to encode.


## -parameters




### -param ppIFrameEncode [out]

A pointer to the newly created frame object.


### -param pArrayIndex [out, optional]

Points to the location where the array index is returned.


### -param pMipLevel [out, optional]

Points to the location where the mip level index is returned.


### -param pSliceIndex [out, optional]

Points to the location where the slice index is returned.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is equivalent to <a href="https://msdn.microsoft.com/1c48f603-e7be-4b0c-a262-0dd01308e868">IWICBitmapEncoder::CreateNewFrame</a>, but returns additional information about the array index, mip level and slice of the newly created frame. In contrast to <b>IWICBitmapEncoder::CreateNewFrame</b>, there is no <a href="https://msdn.microsoft.com/b97caba6-298a-4b36-9f39-9b5440b866c3">IPropertyBag2</a>* parameter because individual DDS frames do not have separate properties.




## -see-also




<a href="https://msdn.microsoft.com/DF14309F-7595-4ABE-BB6E-03D2914CC86D">IWICDdsEncoder</a>



<a href="https://msdn.microsoft.com/2E5755B4-E8DC-40B2-8DA1-B053A261079B">WICDdsParameters</a>
 

 

