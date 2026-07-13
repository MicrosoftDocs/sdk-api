---
UID: NF:shdeprecated.IBrowserService2.v_CheckZoneCrossing
title: IBrowserService2::v_CheckZoneCrossing (shdeprecated.h)
description: Deprecated. Called by the base class to validate a zone crossing when navigating from one page to another.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","v_CheckZoneCrossing method","IBrowserService2.v_CheckZoneCrossing","IBrowserService2::v_CheckZoneCrossing","shdeprecated/IBrowserService2::v_CheckZoneCrossing","shell.IBrowserService2_v_CheckZoneCrossing","v_CheckZoneCrossing","v_CheckZoneCrossing method [Windows Shell]","v_CheckZoneCrossing method [Windows Shell]","IBrowserService2 interface","zone_IBrowserService2_v_CheckZoneCrossing"]
old-location: shell\IBrowserService2_v_CheckZoneCrossing.htm
tech.root: shell
ms.assetid: cc682057-9a84-4b14-bfe3-32b6ada9304c
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],v_CheckZoneCrossing method, IBrowserService2.v_CheckZoneCrossing, IBrowserService2::v_CheckZoneCrossing, shdeprecated/IBrowserService2::v_CheckZoneCrossing, shell.IBrowserService2_v_CheckZoneCrossing, v_CheckZoneCrossing, v_CheckZoneCrossing method [Windows Shell], v_CheckZoneCrossing method [Windows Shell],IBrowserService2 interface, zone_IBrowserService2_v_CheckZoneCrossing
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
req.product: Internet Explorer 5.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService2::v_CheckZoneCrossing
 - shdeprecated/IBrowserService2::v_CheckZoneCrossing
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService2.v_CheckZoneCrossing
---

# IBrowserService2::v_CheckZoneCrossing


## -description

Deprecated. Called by the base class to validate a zone crossing when navigating from one page to another.

## -parameters

### -param pidl [in, out]

Type: <b>LPCITEMIDLIST</b>

The PIDL of the navigation destination.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

