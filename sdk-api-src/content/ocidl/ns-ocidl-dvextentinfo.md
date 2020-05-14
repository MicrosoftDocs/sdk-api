---
UID: NS:ocidl.tagExtentInfo
title: DVEXTENTINFO (ocidl.h)
description: Represents the sizing data used in IViewObjectEx::GetNaturalExtent.
helpviewer_keywords: ["DVEXTENTINFO","DVEXTENTINFO structure [COM]","_ole_DVEXTENTINFO","com.dvextentinfo","ocidl/DVEXTENTINFO"]
old-location: com\dvextentinfo.htm
tech.root: com
ms.assetid: bd603de2-39db-43a1-a391-01dcfedc073f
ms.date: 12/05/2018
ms.keywords: DVEXTENTINFO, DVEXTENTINFO structure [COM], _ole_DVEXTENTINFO, com.dvextentinfo, ocidl/DVEXTENTINFO
f1_keywords:
- ocidl/DVEXTENTINFO
dev_langs:
- c++
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
- OCIdl.h
api_name:
- DVEXTENTINFO
targetos: Windows
req.typenames: DVEXTENTINFO
req.redist: 
ms.custom: 19H1
---

# DVEXTENTINFO structure


## -description


Represents the sizing data used in <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iviewobjectex-getnaturalextent">IViewObjectEx::GetNaturalExtent</a>.


## -struct-fields




### -field cb

The size of the structure, in bytes.


### -field dwExtentMode

Indicates whether the sizing mode is content or integral sizing. See the <a href="/windows/win32/api/ocidl/ne-ocidl-dvextentmode">DVEXTENTMODE</a> enumeration for possible values.


### -field sizelProposed

The proposed size in content sizing or the preferred size in integral sizing.


## -see-also




<a href="/windows/win32/api/ocidl/ne-ocidl-dvextentmode">DVEXTENTMODE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iviewobjectex-getnaturalextent">IViewObjectEx::GetNaturalExtent</a>
 

 

