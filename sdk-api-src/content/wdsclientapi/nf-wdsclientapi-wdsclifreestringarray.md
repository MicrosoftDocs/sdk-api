---
UID: NF:wdsclientapi.WdsCliFreeStringArray
title: WdsCliFreeStringArray function (wdsclientapi.h)
description: This function can be used to free the array of string values that gets allocated by the WdsCliObtainDriverPackages function.
helpviewer_keywords: ["WdsCliFreeStringArray","WdsCliFreeStringArray function [Windows Deployment Services]","wds.wdsclifreestringarray","wdsclientapi/WdsCliFreeStringArray"]
old-location: wds\wdsclifreestringarray.htm
tech.root: wds
ms.assetid: 37d96077-d3f0-4372-955d-f8c071d82230
ms.date: 12/05/2018
ms.keywords: WdsCliFreeStringArray, WdsCliFreeStringArray function [Windows Deployment Services], wds.wdsclifreestringarray, wdsclientapi/WdsCliFreeStringArray
req.header: wdsclientapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WdsClientAPI.lib
req.dll: WdsClientAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsCliFreeStringArray
 - wdsclientapi/WdsCliFreeStringArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsClientAPI.dll
api_name:
 - WdsCliFreeStringArray
---

# WdsCliFreeStringArray function


## -description

This function can be used to free the array of string values that gets allocated by the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliobtaindriverpackages">WdsCliObtainDriverPackages</a> function.

## -parameters

### -param ppwszArray [in, out, optional]

Pointer to the array of string values being freed.

### -param ulCount [in]

Number of strings in the array that is pointed to by <i>ppwszArray</i>.

## -returns

If the function succeeds, the return is <b>S_OK</b>.