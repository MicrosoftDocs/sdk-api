---
UID: NF:segment.IMSVidStreamBufferSinkEvent3.LicenseChange
title: IMSVidStreamBufferSinkEvent3::LicenseChange method
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\imsvidstreambuffersinkevent3_licensechange.htm
old-project: mstv
ms.assetid: 2477f082-50a6-4b4b-89ba-ccf4c8894a4b
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMSVidStreamBufferSinkEvent3, IMSVidStreamBufferSinkEvent3 interface [Microsoft TV Technologies], LicenseChange method, IMSVidStreamBufferSinkEvent3::LicenseChange, IMSVidStreamBufferSinkEvent3LicenseChange, LicenseChange method [Microsoft TV Technologies], LicenseChange method [Microsoft TV Technologies], IMSVidStreamBufferSinkEvent3 interface, LicenseChange,IMSVidStreamBufferSinkEvent3.LicenseChange, mstv.imsvidstreambuffersinkevent3_licensechange, segment/IMSVidStreamBufferSinkEvent3::LicenseChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidStreamBufferSinkEvent3.LicenseChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMSVidStreamBufferSinkEvent3::LicenseChange method


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>LicenseChange</b> method is called when the license for the content changes.


## -parameters




### -param dwProt [in]

Specifies the new license as a member of the <a href="https://msdn.microsoft.com/190b8483-91c8-4fe4-8189-637749393151">ProtType</a> enumeration.


## -returns



Return S_OK or an error code.




## -see-also




<a href="https://msdn.microsoft.com/3d76be50-0e67-4e23-8ce0-8ac9f4ad0c1c">IMSVidStreamBufferSinkEvent3 Interface</a>
 

 

