---
UID: NE:d2d1effects.D2D1_HISTOGRAM_PROP
title: D2D1_HISTOGRAM_PROP
author: windows-sdk-content
description: Identifiers for properties of the Histogram effect.
old-location: direct2d\d2d1_histogram_prop.htm
old-project: direct2d
ms.assetid: 7CBF945C-3BBA-4243-A76B-5CDAC045E79C
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D2D1_HISTOGRAM_PROP, D2D1_HISTOGRAM_PROP enumeration [Direct2D], D2D1_HISTOGRAM_PROP_CHANNEL_SELECT, D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT, D2D1_HISTOGRAM_PROP_NUM_BINS, d2d1effects/D2D1_HISTOGRAM_PROP, d2d1effects/D2D1_HISTOGRAM_PROP_CHANNEL_SELECT, d2d1effects/D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT, d2d1effects/D2D1_HISTOGRAM_PROP_NUM_BINS, direct2d.d2d1_histogram_prop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effects.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: D2D1_HISTOGRAM_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_HISTOGRAM_PROP
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# D2D1_HISTOGRAM_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/en-us/library/Hh706340(v=VS.85).aspx">Histogram effect</a>.
        


## -enum-fields




### -field D2D1_HISTOGRAM_PROP_NUM_BINS

Specifies the number of bins used for the histogram. The range of intensity values that fall into a particular bucket depend on the number of specified buckets. 
          

The type is UINT32.

The default is 256.


### -field D2D1_HISTOGRAM_PROP_CHANNEL_SELECT

Specifies the channel used to generate the histogram. This effect has a single data output corresponding to the specified channel.
          

The type is <a href="https://msdn.microsoft.com/en-us/library/Dn934224(v=VS.85).aspx">D2D1_CHANNEL_SELECTOR</a>.

The default is D2D1_CHANNEL_SELECTOR_R.


### -field D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT

The output array.
          

The type is FLOAT[].


### -field D2D1_HISTOGRAM_PROP_FORCE_DWORD



