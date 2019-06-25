---
UID: NS:strmif.REGPINMEDIUM
title: REGPINMEDIUM (strmif.h)
author: windows-sdk-content
description: The REGPINMEDIUM structure describes a pin medium for registration through the IFilterMapper2 interface.
old-location: dshow\regpinmedium.htm
tech.root: DirectShow
ms.assetid: ed5614fe-bfeb-4ddf-a626-b14080f45b33
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: REGPINMEDIUM, REGPINMEDIUM structure [DirectShow], REGPINMEDIUMStructure, dshow.regpinmedium, strmif/REGPINMEDIUM
ms.topic: struct
f1_keywords: ["strmif/REGPINMEDIUM"]
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - REGPINMEDIUM
product: Windows
targetos: Windows
req.typenames: REGPINMEDIUM
req.redist: 
ms.custom: 19H1
---

# REGPINMEDIUM structure


## -description



The <code>REGPINMEDIUM</code> structure describes a pin medium for registration through the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> interface.




## -struct-fields




### -field clsMedium

GUID that specifies the medium.


### -field dw1

Variable of type <b>DWORD</b> that specifies the instance of this medium. This is necessary when two identical devices are present on the host system.


### -field dw2

Not used.


## -remarks



A <i>medium</i> identifies a hardware path of communication that exists within a single hardware device or between two devices. Register mediums if your filter is built on kernel streaming pins and needs to connect to other such filters.

This structure is equivalent to the <a href="https://docs.microsoft.com/previous-versions/ff563538(v=vs.85)">KSPIN_MEDIUM</a> structure, which is used by kernel streaming drivers.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/ksmultiple-item">KSMULTIPLE_ITEM</a>
 

 

