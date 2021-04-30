---
UID: NC:ddrawint.PDD_MOCOMPCB_ENDFRAME
title: PDD_MOCOMPCB_ENDFRAME (ddrawint.h)
description: The DdMoCompEndFrame callback function completes a decoded frame.
helpviewer_keywords: ["DdMoCompEndFrame","DdMoCompEndFrame callback function [Display Devices]","PDD_MOCOMPCB_ENDFRAME","PDD_MOCOMPCB_ENDFRAME callback","ddfncs_24cad2ef-0770-46d5-a3f3-a4565ec66626.xml","ddrawint/DdMoCompEndFrame","display.ddmocompendframe"]
old-location: display\ddmocompendframe.htm
tech.root: display
ms.assetid: 3589f003-32fc-44c4-867a-abf54f347de9
ms.date: 12/05/2018
ms.keywords: DdMoCompEndFrame, DdMoCompEndFrame callback function [Display Devices], PDD_MOCOMPCB_ENDFRAME, PDD_MOCOMPCB_ENDFRAME callback, ddfncs_24cad2ef-0770-46d5-a3f3-a4565ec66626.xml, ddrawint/DdMoCompEndFrame, display.ddmocompendframe
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Desktop
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDD_MOCOMPCB_ENDFRAME
 - ddrawint/PDD_MOCOMPCB_ENDFRAME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdMoCompEndFrame
---

## -description

The <b>DdMoCompEndFrame</b> callback function completes a decoded frame.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_endmocompframedata">DD_ENDMOCOMPFRAMEDATA</a> structure that contains the information needed to complete the decoded frame.

## -returns

<b>DdMoCompEndFrame</b> returns one of the following callback codes:

## -remarks

DirectDraw drivers that support motion compensation must implement <b>DdMoCompEndFrame</b>.

DirectDraw ensures that begin and end frames will be properly paired.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_endmocompframedata">DD_ENDMOCOMPFRAMEDATA</a>