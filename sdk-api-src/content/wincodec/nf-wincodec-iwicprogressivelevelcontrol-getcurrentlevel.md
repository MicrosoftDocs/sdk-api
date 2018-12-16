---
UID: NF:wincodec.IWICProgressiveLevelControl.GetCurrentLevel
title: IWICProgressiveLevelControl::GetCurrentLevel
author: windows-sdk-content
description: Gets the decoder's current progressive level.
old-location: wic\_wic_codec_iwicprogressivelevelcontrol_getcurrentlevel.htm
tech.root: wic
ms.assetid: c6f848a0-e373-4344-8923-3ad77165ef71
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCurrentLevel, GetCurrentLevel method [Windows Imaging Component], GetCurrentLevel method [Windows Imaging Component],IWICProgressiveLevelControl interface, IWICProgressiveLevelControl interface [Windows Imaging Component],GetCurrentLevel method, IWICProgressiveLevelControl.GetCurrentLevel, IWICProgressiveLevelControl::GetCurrentLevel, _wic_codec_iwicprogressivelevelcontrol_getcurrentlevel, wic._wic_codec_iwicprogressivelevelcontrol_getcurrentlevel, wincodec/IWICProgressiveLevelControl::GetCurrentLevel
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
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
 - IWICProgressiveLevelControl.GetCurrentLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICProgressiveLevelControl::GetCurrentLevel


## -description


Gets the decoder's current progressive level.


## -parameters




### -param pnLevel [out, retval]

Type: <b>UINT*</b>

Indicates the current level specified.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The level always defaults to the highest progressive level. In order to decode a lower progressive level, <a href="https://msdn.microsoft.com/b4a2c279-385d-4177-bd8f-a49f545c692a">SetCurrentLevel</a> must first be called.




## -see-also




<a href="https://msdn.microsoft.com/d77244bc-b9d4-4b7d-b718-4ee38de46614">IWICProgressiveLevelControl</a>



<a href="https://msdn.microsoft.com/d22c2c59-0fa1-4452-93f1-dbf151033714">Progressive Decoding Overview</a>
 

 

