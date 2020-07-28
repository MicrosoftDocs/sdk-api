---
UID: NE:shcore.__unnamed_enum_0
title: BSOS_OPTIONS (shcore.h)
description: Specifies the behavior of a RandomAccessStream that encapsulates a Component Object Model (COM) IStream.
helpviewer_keywords: ["BSOS_DEFAULT","BSOS_OPTIONS","BSOS_OPTIONS enumeration [Windows Runtime]","BSOS_PREFERDESTINATIONSTREAM","shcore/BSOS_DEFAULT","shcore/BSOS_OPTIONS","shcore/BSOS_PREFERDESTINATIONSTREAM","winrt.bsos_options"]
old-location: winrt\bsos_options.htm
tech.root: WinRT
ms.assetid: C51D945B-37C6-44CB-BF80-5FA62EE1F477
ms.date: 12/05/2018
ms.keywords: BSOS_DEFAULT, BSOS_OPTIONS, BSOS_OPTIONS enumeration [Windows Runtime], BSOS_PREFERDESTINATIONSTREAM, shcore/BSOS_DEFAULT, shcore/BSOS_OPTIONS, shcore/BSOS_PREFERDESTINATIONSTREAM, winrt.bsos_options
f1_keywords:
- shcore/BSOS_OPTIONS
dev_langs:
- c++
req.header: shcore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
- shcore.h
api_name:
- BSOS_OPTIONS
targetos: Windows
req.typenames: BSOS_OPTIONS
req.redist: 
ms.custom: 19H1
---

# BSOS_OPTIONS enumeration


## -description


Specifies the behavior of a <a href="https://docs.microsoft.com/uwp/api/windows.storage.streams.randomaccessstream">RandomAccessStream</a> that encapsulates a Component Object Model (COM) <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>.


## -enum-fields




### -field BSOS_DEFAULT

When creating a <a href="https://docs.microsoft.com/uwp/api/windows.storage.streams.randomaccessstream">RandomAccessStream</a> over a stream, use the base <a href="https://docs.microsoft.com/previous-versions/hh438400(v=vs.85)">IRandomAccessStream</a> behavior on the <a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ne-wtypes-stgmove">STGM</a> mode from the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-stat">Stat</a> method.


### -field BSOS_PREFERDESTINATIONSTREAM

Use the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream">GetDestinationStream</a> method.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/hh438400(v=vs.85)">IRandomAccessStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>
 

 

