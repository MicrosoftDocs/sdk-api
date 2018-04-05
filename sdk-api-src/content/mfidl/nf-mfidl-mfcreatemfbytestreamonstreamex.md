---
UID: NF:mfidl.MFCreateMFByteStreamOnStreamEx
title: MFCreateMFByteStreamOnStreamEx function
author: windows-driver-content
description: Creates a Microsoft Media Foundation byte stream that wraps an IRandomAccessStream object.
old-location: mf\mfcreatemfbytestreamonstreamex.htm
old-project: medfound
ms.assetid: C16C2A5D-7373-4EA9-A02C-3AF97EA47D34
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: MFCreateMFByteStreamOnStreamEx, MFCreateMFByteStreamOnStreamEx function [Media Foundation], mf.mfcreatemfbytestreamonstreamex, mf.mfcreatemfbytestreamonwinrtstream, mfidl/MFCreateMFByteStreamOnStreamEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFCreateMFByteStreamOnStreamEx
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateMFByteStreamOnStreamEx function


## -description


Creates a Microsoft Media Foundation byte stream that wraps an <a href="https://msdn.microsoft.com/a9a4bd11-8c69-4826-9ea0-6f42421c8367">IRandomAccessStream</a> object.


## -parameters




### -param punkStream [in]

A pointer to the <a href="https://msdn.microsoft.com/a9a4bd11-8c69-4826-9ea0-6f42421c8367">IRandomAccessStream</a> interface.


### -param ppByteStream [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

