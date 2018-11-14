---
UID: NF:mfidl.IMFQualityAdviseLimits.GetMaximumDropMode
title: IMFQualityAdviseLimits::GetMaximumDropMode
author: windows-sdk-content
description: Gets the maximum drop mode.
old-location: mf\imfqualityadviselimits_getmaximumdropmode.htm
tech.root: medfound
ms.assetid: af3d968b-7baf-41d8-afd9-dbf673c1bb71
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetMaximumDropMode, GetMaximumDropMode method [Media Foundation], GetMaximumDropMode method [Media Foundation],IMFQualityAdviseLimits interface, IMFQualityAdviseLimits interface [Media Foundation],GetMaximumDropMode method, IMFQualityAdviseLimits.GetMaximumDropMode, IMFQualityAdviseLimits::GetMaximumDropMode, mf.imfqualityadviselimits_getmaximumdropmode, mfidl/IMFQualityAdviseLimits::GetMaximumDropMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IMFQualityAdviseLimits.GetMaximumDropMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfidl.h
: 
- IMFQualityAdviseLimits.GetMaximumDropMode
: 
---

# IMFQualityAdviseLimits::GetMaximumDropMode


## -description


Gets the maximum <i>drop mode</i>. A higher drop mode means that the object will, if needed, drop samples more aggressively to match the presentation clock.


## -parameters




### -param peDropMode [out]

Receives the maximum drop mode, specified as a member of the <a href="https://msdn.microsoft.com/e40751d2-9abf-4fe6-8829-9b1fbf4531e8">MF_QUALITY_DROP_MODE</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To get the current drop mode, call the <a href="https://msdn.microsoft.com/bb700a3e-837f-4e88-a9b7-294c41143402">IMFQualityAdvise::GetDropMode</a> method. To set the drop mode, call the <a href="https://msdn.microsoft.com/190de66a-6c47-49d5-a8f6-c2fb57a7aee2">IMFQualityAdvise::SetDropMode</a> method.




## -see-also




<a href="https://msdn.microsoft.com/8ef7088c-2f49-4be9-b719-481616e1737d">IMFQualityAdviseLimits</a>
 

 

