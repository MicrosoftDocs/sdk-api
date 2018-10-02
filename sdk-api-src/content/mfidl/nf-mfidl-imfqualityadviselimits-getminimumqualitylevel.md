---
UID: NF:mfidl.IMFQualityAdviseLimits.GetMinimumQualityLevel
title: IMFQualityAdviseLimits::GetMinimumQualityLevel
author: windows-sdk-content
description: Gets the minimum quality level that is supported by the component.
old-location: mf\imfqualityadviselimits_getminimumqualitylevel.htm
tech.root: MedFound
ms.assetid: aea08ae5-4252-4703-964b-afc6bbc01a51
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetMinimumQualityLevel, GetMinimumQualityLevel method [Media Foundation], GetMinimumQualityLevel method [Media Foundation],IMFQualityAdviseLimits interface, IMFQualityAdviseLimits interface [Media Foundation],GetMinimumQualityLevel method, IMFQualityAdviseLimits.GetMinimumQualityLevel, IMFQualityAdviseLimits::GetMinimumQualityLevel, mf.imfqualityadviselimits_getminimumqualitylevel, mfidl/IMFQualityAdviseLimits::GetMinimumQualityLevel
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
 - IMFQualityAdviseLimits.GetMinimumQualityLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFQualityAdviseLimits::GetMinimumQualityLevel


## -description


Gets the minimum quality level that is supported by the component.


## -parameters




### -param peQualityLevel [out]

Receives the minimum quality level, specified as a member of the <a href="https://msdn.microsoft.com/6fe5abbb-c079-4d74-9c75-6fb502054546">MF_QUALITY_LEVEL</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To get the current quality level, call the <a href="https://msdn.microsoft.com/9a2b501e-543d-4ba0-86a1-a55e7d136685">IMFQualityAdvise::GetQualityLevel</a> method. To set the quality level, call the <a href="https://msdn.microsoft.com/f788fd7d-65fc-4917-8d5d-cfaf35a013e7">IMFQualityAdvise::SetQualityLevel</a> method.




## -see-also




<a href="https://msdn.microsoft.com/8ef7088c-2f49-4be9-b719-481616e1737d">IMFQualityAdviseLimits</a>
 

 

