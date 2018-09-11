---
UID: NF:mfmediaengine.IMFMediaEngine.GetBuffered
title: IMFMediaEngine::GetBuffered
author: windows-sdk-content
description: Queries how much resource data the media engine has buffered.
old-location: mf\imfmediaengine_getbuffered.htm
tech.root: medfound
ms.assetid: 38DABEE7-04AF-4542-AF4D-7988C824EA11
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetBuffered, GetBuffered method [Media Foundation], GetBuffered method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetBuffered method, IMFMediaEngine.GetBuffered, IMFMediaEngine::GetBuffered, mf.imfmediaengine_getbuffered, mfmediaengine/IMFMediaEngine::GetBuffered
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngine.GetBuffered
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngine::GetBuffered


## -description


Queries how much resource data the media engine has buffered.


## -parameters




### -param ppBuffered [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/E39646E6-66F4-4413-A84B-43039689AEE7">IMFMediaTimeRange</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method corresponds to the <b>buffered</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

The returned  <a href="https://msdn.microsoft.com/E39646E6-66F4-4413-A84B-43039689AEE7">IMFMediaTimeRange</a> interface represents a list of time ranges. The time ranges indicate which portions of the media resource have been downloaded. The time range list can be empty.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

