---
UID: NF:mfidl.IMFTimecodeTranslate.EndConvertTimecodeToHNS
title: IMFTimecodeTranslate::EndConvertTimecodeToHNS
author: windows-sdk-content
description: Completes an asynchronous request to convert time in Society of Motion Picture and Television Engineers (SMPTE) time code to 100-nanosecond units.
old-location: mf\imftimecodetranslate_endconverttimecodetohns.htm
old-project: medfound
ms.assetid: d1b8b8ba-d03a-4a45-8788-38dbb2be8c6a
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: EndConvertTimecodeToHNS, EndConvertTimecodeToHNS method [Media Foundation], EndConvertTimecodeToHNS method [Media Foundation],IMFTimecodeTranslate interface, IMFTimecodeTranslate interface [Media Foundation],EndConvertTimecodeToHNS method, IMFTimecodeTranslate.EndConvertTimecodeToHNS, IMFTimecodeTranslate::EndConvertTimecodeToHNS, mf.imftimecodetranslate_endconverttimecodetohns, mfidl/IMFTimecodeTranslate::EndConvertTimecodeToHNS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfidl.h
api_name:
-	IMFTimecodeTranslate.EndConvertTimecodeToHNS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTimecodeTranslate::EndConvertTimecodeToHNS


## -description


Completes an asynchronous request to convert time in Society of Motion Picture and Television Engineers (SMPTE) time code to 100-nanosecond units.


## -parameters




### -param pResult [in]

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method.




### -param phnsTime [out]

Receives the converted time.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method after the <a href="https://msdn.microsoft.com/4e25d5e4-b4d7-4ca4-81c9-12c6d712322d">IMFTimecodeTranslate::BeginConvertTimecodeToHNS</a> method completes asynchronously.




## -see-also




<a href="https://msdn.microsoft.com/1d8688a5-d476-457d-a0ad-e4f106ac3484">Calling Asynchronous Methods</a>



<a href="https://msdn.microsoft.com/935ec6b3-12e6-4458-b8a1-ffeb4159d957">IMFTimecodeTranslate</a>



<a href="https://msdn.microsoft.com/9273ff1f-382e-4c58-b571-4852545915b3">MFTIME</a>
 

 

