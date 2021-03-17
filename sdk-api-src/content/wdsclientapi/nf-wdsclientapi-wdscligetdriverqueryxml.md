---
UID: NF:wdsclientapi.WdsCliGetDriverQueryXml
title: WdsCliGetDriverQueryXml function (wdsclientapi.h)
description: This function generates an XML string which can be used to query a WDS server for driver packages using the WdsCliObtainDriverPackagesEx function.
helpviewer_keywords: ["WdsCliGetDriverQueryXml","WdsCliGetDriverQueryXml function [Windows Deployment Services]","wds.wdscligetdriverqueryxml","wdsclientapi/WdsCliGetDriverQueryXml"]
old-location: wds\wdscligetdriverqueryxml.htm
tech.root: wds
ms.assetid: 0E5ABBBD-CD8A-4D0B-9D4B-5044278961D8
ms.date: 12/05/2018
ms.keywords: WdsCliGetDriverQueryXml, WdsCliGetDriverQueryXml function [Windows Deployment Services], wds.wdscligetdriverqueryxml, wdsclientapi/WdsCliGetDriverQueryXml
req.header: wdsclientapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - WdsCliGetDriverQueryXml
 - wdsclientapi/WdsCliGetDriverQueryXml
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
 - WdsCliGetDriverQueryXml
---

# WdsCliGetDriverQueryXml function


## -description

This function generates an XML string which can be used to query a WDS server for driver packages using the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliobtaindriverpackagesex">WdsCliObtainDriverPackagesEx</a> function.  The target OS information section of the WDS driver query XML is generated if the path to the Windows directory of the applied image is specified.

## -parameters

### -param pwszWinDirPath [in, optional]

The path to the Windows directory of the applied image. This parameter is optional. If it is specified,  the section of the WDS driver query XML  for the target operating system is generated.

### -param ppwszDriverQuery [out]

A pointer to a pointer to a string that receives the generated WDS driver query XML. The caller has to free this buffer using "delete\[\]\(\*ppwszDriverQuery\)".

## -returns

If the function succeeds, the return is <b>S_OK</b>.