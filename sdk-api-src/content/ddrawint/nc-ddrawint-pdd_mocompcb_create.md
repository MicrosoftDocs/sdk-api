---
UID: NC:ddrawint.PDD_MOCOMPCB_CREATE
title: PDD_MOCOMPCB_CREATE (ddrawint.h)
description: The DdMoCompCreate callback function notifies the driver that a software decoder will start using motion compensation with the specified GUID.
helpviewer_keywords: ["DdMoCompCreate","DdMoCompCreate callback function [Display Devices]","PDD_MOCOMPCB_CREATE","PDD_MOCOMPCB_CREATE callback","ddfncs_b5650d61-0a79-494a-acd7-231d2e859c30.xml","ddrawint/DdMoCompCreate","display.ddmocompcreate"]
old-location: display\ddmocompcreate.htm
tech.root: display
ms.assetid: 9413108b-f9b5-4d1c-83a9-b663a9f444bf
ms.date: 12/05/2018
ms.keywords: DdMoCompCreate, DdMoCompCreate callback function [Display Devices], PDD_MOCOMPCB_CREATE, PDD_MOCOMPCB_CREATE callback, ddfncs_b5650d61-0a79-494a-acd7-231d2e859c30.xml, ddrawint/DdMoCompCreate, display.ddmocompcreate
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
 - PDD_MOCOMPCB_CREATE
 - ddrawint/PDD_MOCOMPCB_CREATE
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
 - DdMoCompCreate
---

## -description

The <i>DdMoCompCreate</i> callback function notifies the driver that a software decoder will start using motion compensation with the specified GUID.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_createmocompdata">DD_CREATEMOCOMPDATA</a> structure that contains the information required to begin using motion compensation.

## -returns

<i>DdMoCompCreate</i> returns one of the following callback codes:

## -remarks

<i>DdMoCompCreate</i> can be optionally implemented in DirectDraw drivers. It is not required for motion compensation support.

<i>DdMoCompCreate</i> also reports the width, height, and format of the output frame. The driver can fail this call if it cannot support motion compensation with these dimensions.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_createmocompdata">DD_CREATEMOCOMPDATA</a>