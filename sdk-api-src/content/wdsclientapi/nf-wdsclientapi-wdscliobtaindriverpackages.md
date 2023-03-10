---
UID: NF:wdsclientapi.WdsCliObtainDriverPackages
title: WdsCliObtainDriverPackages function (wdsclientapi.h)
description: This function obtains from a WDS image, the driver packages (INF files) that can be used on this computer.
helpviewer_keywords: ["WdsCliObtainDriverPackages","WdsCliObtainDriverPackages function [Windows Deployment Services]","wds.wdscliobtaindriverpackages","wdsclientapi/WdsCliObtainDriverPackages"]
old-location: wds\wdscliobtaindriverpackages.htm
tech.root: wds
ms.assetid: 2fb6bf5a-a46f-4664-be0a-6b4f2563986c
ms.date: 12/05/2018
ms.keywords: WdsCliObtainDriverPackages, WdsCliObtainDriverPackages function [Windows Deployment Services], wds.wdscliobtaindriverpackages, wdsclientapi/WdsCliObtainDriverPackages
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
 - WdsCliObtainDriverPackages
 - wdsclientapi/WdsCliObtainDriverPackages
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
 - WdsCliObtainDriverPackages
---

# WdsCliObtainDriverPackages function


## -description

This function obtains from a WDS image, the driver packages (INF files) that can be used on this computer. The <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifreestringarray">WdsCliFreeStringArray</a> function can be used to free the array of string values allocated by this function.

## -parameters

### -param hImage [in]

A handle to a WDS image.

### -param ppwszServerName [out]

A pointer to a pointer to a string value that receives the IP address of the server hosting the driver packages.

### -param pppwszDriverPackages [out]

An array of string values that are the full paths for the driver packages (INF files.) The Internet Protocol (IP) address, rather than a computer name, is returned as part of the path.  For example, a string value <b>\\172.31.224.245\REMINST\Stores\Drivers\driver.inf</b> in the array gives the full path to driver.inf.

<div class="code"></div>

### -param pulCount [out]

The number of driver packages returned by <i>pppwszDriverPackages</i>.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/Wds/windows-deployment-services-client-functions">Windows Deployment Services Client Functions</a>