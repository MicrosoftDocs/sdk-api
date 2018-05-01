---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetSourceFromByteStream
title: IMFMediaEngineEx::SetSourceFromByteStream method
author: windows-driver-content
description: Opens a media resource from a byte stream.
old-location: mf\imfmediaengineex_setsourcefrombytestream.htm
old-project: medfound
ms.assetid: F643383E-AABA-4F32-BCE9-0AA4FD635A0F
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: IMFMediaEngineEx, IMFMediaEngineEx interface [Media Foundation], SetSourceFromByteStream method, IMFMediaEngineEx::SetSourceFromByteStream, SetSourceFromByteStream method [Media Foundation], SetSourceFromByteStream method [Media Foundation], IMFMediaEngineEx interface, SetSourceFromByteStream,IMFMediaEngineEx.SetSourceFromByteStream, mf.imfmediaengineex_setsourcefrombytestream, mfmediaengine/IMFMediaEngineEx::SetSourceFromByteStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
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
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaEngineEx.SetSourceFromByteStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineEx::SetSourceFromByteStream method


## -description


Opens a media resource from a byte stream.


## -parameters




### -param pByteStream [in]

A pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of the byte stream.


### -param pURL [in]

The URL of the byte stream.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

