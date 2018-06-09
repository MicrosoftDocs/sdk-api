---
UID: NF:strmif.IMPEG2StreamIdMap.EnumStreamIdMap
title: IMPEG2StreamIdMap::EnumStreamIdMap
author: windows-sdk-content
description: The EnumStreamIdMap method returns a collection of all the mapped Stream IDs on this pin.
old-location: dshow\impeg2streamidmap_enumstreamidmap.htm
old-project: DirectShow
ms.assetid: 2c42f042-c9fb-4cb9-90bb-4050a61b18da
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: EnumStreamIdMap, EnumStreamIdMap method [DirectShow], EnumStreamIdMap method [DirectShow],IMPEG2StreamIdMap interface, IMPEG2StreamIdMap interface [DirectShow],EnumStreamIdMap method, IMPEG2StreamIdMap.EnumStreamIdMap, IMPEG2StreamIdMap::EnumStreamIdMap, IMPEG2StreamIdMapEnumStreamIdMap, dshow.impeg2streamidmap_enumstreamidmap, strmif/IMPEG2StreamIdMap::EnumStreamIdMap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMPEG2StreamIdMap.EnumStreamIdMap
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMPEG2StreamIdMap::EnumStreamIdMap


## -description



The <code>EnumStreamIdMap</code> method returns a collection of all the mapped Stream IDs on this pin.




## -parameters




### -param ppIEnumStreamIdMap [in]


<a href="https://msdn.microsoft.com/8bca9255-2bc8-408b-9127-e3fe050fcf01">IEnumStreamIdMap</a> interface pointer that will be set to the returned collection.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



Currently, there is only one stream ID mapped to a given pin, therefore this collection will contain a single item.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/714c6b0e-3885-4026-8a83-06b37cc97d7c">IMPEG2StreamIdMap Interface</a>
 

 

