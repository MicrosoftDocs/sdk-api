---
UID: NE:codecapi.eAVDecHEAACDynamicRangeControl
title: eAVDecHEAACDynamicRangeControl
author: windows-sdk-content
description: Specifies whether an AAC decoder performs dynamic range control.
old-location: dshow\eavdecheaacdynamicrangecontrol.htm
tech.root: DirectShow
ms.assetid: d854093c-4ec8-439c-a1be-c34e3d080616
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: codecapi/eAVDecHEAACDynamicRangeControl, codecapi/eAVDecHEAACDynamicRangeControl_OFF, codecapi/eAVDecHEAACDynamicRangeControl_ON, dshow.eavdecheaacdynamicrangecontrol, eAVDecHEAACDynamicRangeControl, eAVDecHEAACDynamicRangeControl enumeration [DirectShow], eAVDecHEAACDynamicRangeControl_OFF, eAVDecHEAACDynamicRangeControl_ON
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVDecHEAACDynamicRangeControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# eAVDecHEAACDynamicRangeControl enumeration


## -description


Specifies whether an AAC decoder performs dynamic range control. This enumeration is used with the <a href="https://msdn.microsoft.com/b7cf092a-6bb8-454c-a78c-fb2334ac4820">AVDecHEAACDynamicRangeControl</a> property.


## -enum-fields




### -field eAVDecHEAACDynamicRangeControl_OFF

The decoder does not apply dynamic range control.


### -field eAVDecHEAACDynamicRangeControl_ON

The decoder applies dynamic range control to any AAC stream that contains an extension payload of type EXT_DYNAMIC_RANGE, as defined in ISO/IEC 14496-3 (Table 4.105, "Values of the extension_type field").


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd311953(v=VS.85).aspx">ICodecAPI Interface</a>
 

 

