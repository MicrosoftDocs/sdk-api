---
UID: NF:mftransform.IMFTransform.GetStreamLimits
title: IMFTransform::GetStreamLimits
author: windows-sdk-content
description: Gets the minimum and maximum number of input and output streams for this Media Foundation transform (MFT).
old-location: mf\imftransform_getstreamlimits.htm
old-project: medfound
ms.assetid: 4d9585f0-5818-4e7f-925c-4c50ae6a6edc
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: 4d9585f0-5818-4e7f-925c-4c50ae6a6edc, GetStreamLimits, GetStreamLimits method [Media Foundation], GetStreamLimits method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetStreamLimits method, IMFTransform.GetStreamLimits, IMFTransform::GetStreamLimits, mf.imftransform_getstreamlimits, mftransform/IMFTransform::GetStreamLimits
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTransform.GetStreamLimits
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTransform::GetStreamLimits


## -description



          Gets the minimum and maximum number of input and output streams for this Media Foundation transform (MFT).
        


## -parameters




### -param pdwInputMinimum [out]


            Receives the minimum number of input streams.
          


### -param pdwInputMaximum [out]


            Receives the maximum number of input streams. If there is no maximum, receives the value <b>MFT_STREAMS_UNLIMITED</b>.
          


### -param pdwOutputMinimum [out]


            Receives the minimum number of output streams.
          


### -param pdwOutputMaximum [out]


            Receives the maximum number of output streams. If there is no maximum, receives the value <b>MFT_STREAMS_UNLIMITED</b>.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        If the MFT has a fixed number of streams, the minimum and maximum values are the same.
      


        It is not recommended to create an MFT that supports zero inputs or zero outputs. An MFT with no inputs or no outputs may not be compatible with the rest of the Media Foundation pipeline. You should create a Media Foundation sink or source for this purpose instead.
      


        When an MFT is first created, it is not guaranteed to have the minimum number of streams. To find the actual number of streams, call <a href="https://msdn.microsoft.com/491f7f44-fcac-4236-ba5c-e5705267c6c2">IMFTransform::GetStreamCount</a>.
      


        This method should not be called with <b>NULL</b> parameters, although in practice some implementations may allow <b>NULL</b> parameters.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetStreamLimits</b>. See <a href="https://msdn.microsoft.com/library/Bb250374(v=VS.85).aspx">Creating Hybrid DMO/MFT Objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

