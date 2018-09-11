---
UID: NF:wincodec.IWICDevelopRaw.QueryRawCapabilitiesInfo
title: IWICDevelopRaw::QueryRawCapabilitiesInfo
author: windows-sdk-content
description: Retrieves information about which capabilities are supported for a raw image.
old-location: wic\_wic_codec_iwicdevelopraw_queryrawcapabilitiesinfo.htm
tech.root: wic
ms.assetid: a16ada3c-34ae-47ce-9660-90e50d78802a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],QueryRawCapabilitiesInfo method, IWICDevelopRaw.QueryRawCapabilitiesInfo, IWICDevelopRaw::QueryRawCapabilitiesInfo, QueryRawCapabilitiesInfo, QueryRawCapabilitiesInfo method [Windows Imaging Component], QueryRawCapabilitiesInfo method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_queryrawcapabilitiesinfo, wic._wic_codec_iwicdevelopraw_queryrawcapabilitiesinfo, wincodec/IWICDevelopRaw::QueryRawCapabilitiesInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IWICDevelopRaw.QueryRawCapabilitiesInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICDevelopRaw::QueryRawCapabilitiesInfo


## -description


Retrieves information about which capabilities are supported for a raw image.


## -parameters




### -param pInfo [out]

Type: <b><a href="https://msdn.microsoft.com/1466cd90-8eab-4c5c-bb77-c75d35fe586b">WICRawCapabilitiesInfo</a>*</b>

A pointer that receives <a href="https://msdn.microsoft.com/1466cd90-8eab-4c5c-bb77-c75d35fe586b">WICRawCapabilitiesInfo</a> that provides the capabilities supported by the raw image.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



It is recommended that a codec report that a capability is supported even if the results at the outer range limits are not of perfect quality.



