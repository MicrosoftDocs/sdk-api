---
UID: NE:d2d1_1.D2D1_UNIT_MODE
title: D2D1_UNIT_MODE (d2d1_1.h)
author: windows-sdk-content
description: Specifies how units in Direct2D will be interpreted.
old-location: direct2d\__d2d1_unit_mode.htm
tech.root: Direct2D
ms.assetid: 1ba11761-f3e9-4996-8494-384db5bddc99
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D2D1_UNIT_MODE, D2D1_UNIT_MODE enumeration [Direct2D], D2D1_UNIT_MODE_DIPS, D2D1_UNIT_MODE_PIXELS, d2d1_1/D2D1_UNIT_MODE, d2d1_1/D2D1_UNIT_MODE_DIPS, d2d1_1/D2D1_UNIT_MODE_PIXELS, direct2d.__d2d1_unit_mode
ms.topic: enum
f1_keywords: ["d2d1_1/D2D1_UNIT_MODE"]
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - D2d1_1.h
api_name:
 - D2D1_UNIT_MODE
product: Windows
targetos: Windows
req.typenames: D2D1_UNIT_MODE
req.redist: 
ms.custom: 19H1
---

# D2D1_UNIT_MODE enumeration


## -description


Specifies how units in Direct2D will be interpreted.


## -enum-fields




### -field D2D1_UNIT_MODE_DIPS

Units will be interpreted as device-independent pixels (1/96").


### -field D2D1_UNIT_MODE_PIXELS

Units will be interpreted as pixels.


### -field D2D1_UNIT_MODE_FORCE_DWORD




## -remarks



Setting the unit mode to <b>D2D1_UNIT_MODE_PIXELS</b> is similar to setting the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a> dots per inch (dpi) to 96. However, Direct2D still checks the dpi to determine the threshold for enabling vertical antialiasing for text, and when the unit mode is restored, the dpi will be remembered.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-getunitmode">ID2D1DeviceContext::GetUnitMode</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode">ID2D1DeviceContext::SetUnitMode</a>
 

 

