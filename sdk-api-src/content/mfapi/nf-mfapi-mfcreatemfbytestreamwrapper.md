---
UID: NF:mfapi.MFCreateMFByteStreamWrapper
title: MFCreateMFByteStreamWrapper function
author: windows-sdk-content
description: Creates a wrapper for a byte stream.
old-location: mf\mfcreatemfbytestreamwrapper.htm
tech.root: medfound
ms.assetid: F6A9603D-39C8-4039-BAA0-81557CE29078
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: MFCreateMFByteStreamWrapper, MFCreateMFByteStreamWrapper function [Media Foundation], mf.mfcreatemfbytestreamwrapper, mfapi/MFCreateMFByteStreamWrapper
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateMFByteStreamWrapper
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateMFByteStreamWrapper function


## -description


Creates a wrapper for a byte stream.


## -parameters




### -param pStream [in]

A pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of the original byte stream.


### -param ppStreamWrapper [in]

Receives a pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of the wrapper. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> methods on the wrapper call directly through to the original byte stream, except for the <a href="https://msdn.microsoft.com/d5f704ab-fa3f-4a53-9b97-eb48a75e481b">IMFByteStream::Close</a> method. Calling <b>Close</b> on the wrapper closes the wrapper object, but leaves the original byte stream open.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

