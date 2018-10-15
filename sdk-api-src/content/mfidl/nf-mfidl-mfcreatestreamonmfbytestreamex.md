---
UID: NF:mfidl.MFCreateStreamOnMFByteStreamEx
title: MFCreateStreamOnMFByteStreamEx function
author: windows-sdk-content
description: Creates an IRandomAccessStream object that wraps a Microsoft Media Foundation byte stream.
old-location: mf\mfcreatestreamonmfbytestreamex.htm
tech.root: medfound
ms.assetid: 5D43889B-6430-4057-87E8-B8501B52E4A5
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: MFCreateStreamOnMFByteStreamEx, MFCreateStreamOnMFByteStreamEx function [Media Foundation], mf.mfcreatestreamonmfbytestreamex, mf.mfcreatewinrtstreamonmfbytestream, mfidl/MFCreateStreamOnMFByteStreamEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - MFCreateStreamOnMFByteStreamEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateStreamOnMFByteStreamEx function


## -description


Creates an <a href="https://msdn.microsoft.com/a9a4bd11-8c69-4826-9ea0-6f42421c8367">IRandomAccessStream</a> object that wraps a Microsoft Media Foundation byte stream.


## -parameters




### -param pByteStream [in]

A pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of the Media Foundation byte stream.


### -param riid [in]

The interface identifier (IID) of the interface being requested. 


### -param ppv [out]

Receives a pointer to the requested interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The returned byte stream object exposes the <a href="https://msdn.microsoft.com/102a1dff-8419-4f86-a145-53ce3d0123f5">IMFGetService</a> interface. To get the original <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> pointer, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> using the service identifier <b>MF_WRAPPED_OBJECT</b>.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

