---
UID: NF:mfidl.IMFByteStreamCacheControl2.IsBackgroundTransferActive
title: IMFByteStreamCacheControl2::IsBackgroundTransferActive
author: windows-sdk-content
description: Queries whether background transfer is active.
old-location: mf\imfbytestreamcachecontrol2_isbackgroundtransferactive.htm
tech.root: medfound
ms.assetid: FC08E5E8-A7E0-461C-B70C-B1273FCDD1A0
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IMFByteStreamCacheControl2 interface [Media Foundation],IsBackgroundTransferActive method, IMFByteStreamCacheControl2.IsBackgroundTransferActive, IMFByteStreamCacheControl2::IsBackgroundTransferActive, IsBackgroundTransferActive, IsBackgroundTransferActive method [Media Foundation], IsBackgroundTransferActive method [Media Foundation],IMFByteStreamCacheControl2 interface, mf.imfbytestreamcachecontrol2_isbackgroundtransferactive, mfidl/IMFByteStreamCacheControl2::IsBackgroundTransferActive
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFByteStreamCacheControl2.IsBackgroundTransferActive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFByteStreamCacheControl2::IsBackgroundTransferActive


## -description


Queries whether background transfer is active.


## -parameters




### -param pfActive [out]

Receives the value <b>TRUE</b> if background transfer is currently active, or <b>FALSE</b> otherwise.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Background transfer might stop because the cache limit was reached (see <a href="https://msdn.microsoft.com/1DDC3D76-E28B-4B8C-B2CD-FE77E840D949">IMFByteStreamCacheControl2::SetCacheLimit</a>) or because the <a href="https://msdn.microsoft.com/9f0f7102-c839-4e92-a798-5ea31ceba013">IMFByteStreamCacheControl::StopBackgroundTransfer</a> method was called.




## -see-also




<a href="https://msdn.microsoft.com/A901F679-B6F2-4DB7-8EFC-EA61249B64FB">IMFByteStreamCacheControl2</a>
 

 

