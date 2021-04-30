---
UID: NC:ddrawint.PDD_PALCB_SETENTRIES
title: PDD_PALCB_SETENTRIES (ddrawint.h)
description: The DdSetEntries callback function updates the palette entries in the specified palette.
helpviewer_keywords: ["DdSetEntries","DdSetEntries callback function [Display Devices]","PDD_PALCB_SETENTRIES","PDD_PALCB_SETENTRIES callback","ddfncs_904cb314-1d34-4ace-b1ba-92e25ed8f293.xml","ddrawint/DdSetEntries","display.ddsetentries"]
old-location: display\ddsetentries.htm
tech.root: display
ms.assetid: 41b0b433-288d-4d7b-b961-2789b2540761
ms.date: 12/05/2018
ms.keywords: DdSetEntries, DdSetEntries callback function [Display Devices], PDD_PALCB_SETENTRIES, PDD_PALCB_SETENTRIES callback, ddfncs_904cb314-1d34-4ace-b1ba-92e25ed8f293.xml, ddrawint/DdSetEntries, display.ddsetentries
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
 - PDD_PALCB_SETENTRIES
 - ddrawint/PDD_PALCB_SETENTRIES
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
 - DdSetEntries
---

## -description

The <i>DdSetEntries</i> callback function updates the palette entries in the specified palette.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_setentriesdata">DD_SETENTRIESDATA</a> structure that contains the information required to set the palette's entries.

## -returns

<i>DdSetEntries</i> returns one of the following callback codes:

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_setentriesdata">DD_SETENTRIESDATA</a>