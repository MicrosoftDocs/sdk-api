---
UID: NF:mfidl.MFCreateStreamOnMFByteStream
title: MFCreateStreamOnMFByteStream function
author: windows-driver-content
description: Returns an IStream pointer that wraps a Microsoft Media Foundation byte stream.
old-location: mf\mfcreatestreamonmfbytestream.htm
old-project: medfound
ms.assetid: 97C72B89-2E57-494E-AEB8-41125B3D740E
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: MFCreateStreamOnMFByteStream, MFCreateStreamOnMFByteStream function [Media Foundation], mf.mfcreatestreamonmfbytestream, mfidl/MFCreateStreamOnMFByteStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
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
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFCreateStreamOnMFByteStream
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateStreamOnMFByteStream function


## -description


Returns an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> pointer that wraps a Microsoft Media Foundation byte stream.


## -parameters




### -param pByteStream [in]

A pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of the Media Foundation byte stream.


### -param ppStream [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function enables an application to pass a Media Foundation byte stream to an API that takes an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> pointer.




## -see-also




<a href="https://msdn.microsoft.com/5ffd370a-ccc5-4229-b214-e07847287415">MFCreateMFByteStreamOnStream</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

