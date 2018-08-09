---
UID: NF:wmcontainer.MFCreateWMVEncoderActivate
title: MFCreateWMVEncoderActivate function
author: windows-sdk-content
description: Creates an activation object that can be used to create a Windows Media Video (WMV) encoder.
old-location: mf\mfcreatewmvencoderactivate.htm
old-project: medfound
ms.assetid: f818dba1-e28f-4fd4-813d-33f638d979d7
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MFCreateWMVEncoderActivate, MFCreateWMVEncoderActivate function [Media Foundation], f818dba1-e28f-4fd4-813d-33f638d979d7, mf.mfcreatewmvencoderactivate, wmcontainer/MFCreateWMVEncoderActivate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFSINK_WMDRMACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateWMVEncoderActivate
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# MFCreateWMVEncoderActivate function


## -description


Creates an activation object that can be used to create a Windows Media Video (WMV) encoder.
        


## -parameters




### -param pMediaType

A pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface. This parameter specifies the encoded output format.


### -param pEncodingConfigurationProperties

A pointer to the <b>IPropertyStore</b> interface of a property store that contains encoding parameters. Encoding parameters for the WMV encoder are defined in the header file wmcodecdsp.h. If you have an ASF ContentInfo object that contains an ASF profile object with all the streams for the output file, you can get the property store by calling <a href="https://msdn.microsoft.com/e77a5564-82bc-4c1d-9fb8-84ab484c4ca8">IMFASFContentInfo::GetEncodingConfigurationPropertyStore</a>.
          


### -param ppActivate

Receives a pointer to the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface. Use this interface to create the encoder. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/767d5f1c-2b8d-43b6-916b-035129e93204">Activation Objects</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

