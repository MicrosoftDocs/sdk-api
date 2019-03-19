---
UID: NF:mfidl.MFCreateMFByteStreamOnStream
title: MFCreateMFByteStreamOnStream function (mfidl.h)
author: windows-sdk-content
description: Creates a Microsoft Media Foundation byte stream that wraps an IStream pointer.
old-location: mf\mfcreatemfbytestreamonstream.htm
tech.root: medfound
ms.assetid: 5ffd370a-ccc5-4229-b214-e07847287415
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MFCreateMFByteStreamOnStream, MFCreateMFByteStreamOnStream function [Media Foundation], mf.mfcreatemfbytestreamonstream, mfidl/MFCreateMFByteStreamOnStream
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - MFCreateMFByteStreamOnStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateMFByteStreamOnStream function


## -description


Creates a Microsoft Media Foundation byte stream that wraps an <b>IStream</b> pointer.


## -parameters




### -param pStream [in]

A pointer to the <b>IStream</b> interface.


### -param ppByteStream [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface. The caller must release the interface.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This function enables applications to pass an <b>IStream</b> object to a Media Foundation API that takes an <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> pointer.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

