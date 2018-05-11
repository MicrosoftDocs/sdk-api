---
UID: NE:vptype._AMVP_SELECT_FORMAT_BY
title: "_AMVP_SELECT_FORMAT_BY"
author: windows-driver-content
description: Specifies the criteria that the Overlay Mixer Filter should use to select the video format.
old-location: dshow\amvp_select_format_by.htm
old-project: DirectShow
ms.assetid: 98f60199-630b-4759-a0fa-86292713a36d
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: AMVP_BEST_BANDWIDTH, AMVP_DO_NOT_CARE, AMVP_INPUT_SAME_AS_OUTPUT, AMVP_SELECT_FORMAT_BY, AMVP_SELECT_FORMAT_BY , AMVP_SELECT_FORMAT_BY enumeration [DirectShow], AMVP_SELECT_FORMAT_BYEnumeration, _AMVP_SELECT_FORMAT_BY, dshow.amvp_select_format_by, vptype/AMVP_BEST_BANDWIDTH, vptype/AMVP_DO_NOT_CARE, vptype/AMVP_INPUT_SAME_AS_OUTPUT, vptype/AMVP_SELECT_FORMAT_BY
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: vptype.h
req.include-header: 
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
req.typenames: AMVP_SELECT_FORMAT_BY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	vptype.h
api_name:
-	AMVP_SELECT_FORMAT_BY
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# _AMVP_SELECT_FORMAT_BY enumeration


## -description



Specifies the criteria that the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer Filter</a> should use to select the video format.




## -enum-fields




### -field AMVP_DO_NOT_CARE


            Format does not matter.
          


### -field AMVP_BEST_BANDWIDTH


            Use the largest bandwidth.
          


### -field AMVP_INPUT_SAME_AS_OUTPUT


            Use the same input format as output format.
          


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

