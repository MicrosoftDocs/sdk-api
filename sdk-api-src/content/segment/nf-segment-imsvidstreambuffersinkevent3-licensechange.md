---
UID: NF:segment.IMSVidStreamBufferSinkEvent3.LicenseChange
title: IMSVidStreamBufferSinkEvent3::LicenseChange (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.helpviewer_keywords: ["IMSVidStreamBufferSinkEvent3 interface [Microsoft TV Technologies]","LicenseChange method","IMSVidStreamBufferSinkEvent3.LicenseChange","IMSVidStreamBufferSinkEvent3::LicenseChange","IMSVidStreamBufferSinkEvent3LicenseChange","LicenseChange","LicenseChange method [Microsoft TV Technologies]","LicenseChange method [Microsoft TV Technologies]","IMSVidStreamBufferSinkEvent3 interface","mstv.imsvidstreambuffersinkevent3_licensechange","segment/IMSVidStreamBufferSinkEvent3::LicenseChange"]
old-location: mstv\imsvidstreambuffersinkevent3_licensechange.htm
tech.root: mstv
ms.assetid: 2477f082-50a6-4b4b-89ba-ccf4c8894a4b
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSinkEvent3 interface [Microsoft TV Technologies],LicenseChange method, IMSVidStreamBufferSinkEvent3.LicenseChange, IMSVidStreamBufferSinkEvent3::LicenseChange, IMSVidStreamBufferSinkEvent3LicenseChange, LicenseChange, LicenseChange method [Microsoft TV Technologies], LicenseChange method [Microsoft TV Technologies],IMSVidStreamBufferSinkEvent3 interface, mstv.imsvidstreambuffersinkevent3_licensechange, segment/IMSVidStreamBufferSinkEvent3::LicenseChange
f1_keywords:
- segment/IMSVidStreamBufferSinkEvent3.LicenseChange
dev_langs:
- c++
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
- segment.h
api_name:
- IMSVidStreamBufferSinkEvent3.LicenseChange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidStreamBufferSinkEvent3::LicenseChange


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>LicenseChange</b> method is called when the license for the content changes.


## -parameters




### -param dwProt [in]

Specifies the new license as a member of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/ne-encdec-prottype">ProtType</a> enumeration.


## -returns



Return S_OK or an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidstreambuffersinkevent3">IMSVidStreamBufferSinkEvent3 Interface</a>
 

 

