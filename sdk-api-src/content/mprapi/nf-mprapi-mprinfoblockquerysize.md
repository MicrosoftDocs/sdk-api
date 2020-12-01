---
UID: NF:mprapi.MprInfoBlockQuerySize
title: MprInfoBlockQuerySize function (mprapi.h)
description: The MprInfoBlockQuerySize function returns the returns the size of the information header.
helpviewer_keywords: ["MprInfoBlockQuerySize","MprInfoBlockQuerySize function [RAS]","_mpr_mprinfoblockquerysize","mprapi/MprInfoBlockQuerySize","rras.mprinfoblockquerysize"]
old-location: rras\mprinfoblockquerysize.htm
tech.root: RRAS
ms.assetid: cac491c9-3486-4eba-afe9-9e18f50c0643
ms.date: 12/05/2018
ms.keywords: MprInfoBlockQuerySize, MprInfoBlockQuerySize function [RAS], _mpr_mprinfoblockquerysize, mprapi/MprInfoBlockQuerySize, rras.mprinfoblockquerysize
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprInfoBlockQuerySize
 - mprapi/MprInfoBlockQuerySize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprInfoBlockQuerySize
---

# MprInfoBlockQuerySize function


## -description

The 
<b>MprInfoBlockQuerySize</b> function returns the returns the size of the information header.

## -parameters

### -param lpHeader [in]

Pointer to the information header for which to return the size.

## -returns

<b>MprInfoBlockQuerySize</b> returns the size of the information header.

## -see-also

<a href="/windows/desktop/RRAS/understanding-mprinfo-functions-and-information-headers">MprInfo Functions and Information Headers</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockadd">MprInfoBlockAdd</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockremove">MprInfoBlockRemove</a>