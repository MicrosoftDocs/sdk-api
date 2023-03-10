---
UID: NF:cfapi.CfGetPlaceholderStateFromFileInfo
title: CfGetPlaceholderStateFromFileInfo function (cfapi.h)
description: Gets a set of placeholder states based on the various information of the file.
helpviewer_keywords: ["CfGetPlaceholderStateFromFileInfo","CfGetPlaceholderStateFromFileInfo function","cfapi/CfGetPlaceholderStateFromFileInfo","cloudApi.cfgetplaceholderstatefromfileinfo"]
old-location: cloudapi\cfgetplaceholderstatefromfileinfo.htm
tech.root: cloudapi
ms.assetid: 33DB8FAC-D2C9-4BBB-8505-1D9A680EA2BF
ms.date: 12/05/2018
ms.keywords: CfGetPlaceholderStateFromFileInfo, CfGetPlaceholderStateFromFileInfo function, cfapi/CfGetPlaceholderStateFromFileInfo, cloudApi.cfgetplaceholderstatefromfileinfo
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CfGetPlaceholderStateFromFileInfo
 - cfapi/CfGetPlaceholderStateFromFileInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfGetPlaceholderStateFromFileInfo
---

# CfGetPlaceholderStateFromFileInfo function


## -description

Gets a set of placeholder states based on the various information of the file.

## -parameters

### -param InfoBuffer [in]

An info buffer about the file.

### -param InfoClass [in]

An info class so the function knows how to interpret the <i>InfoBuffer</i>.

## -returns

Can include <a href="/windows/desktop/api/cfapi/ne-cfapi-cf_placeholder_state">CF_PLACEHOLDER_STATE</a>; The placeholder state.

## -remarks

The input is a buffer containing information returned by <a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>, and the corresponding <i>InfoClass</i> so the API knows how to interpret the buffer.


Not all information classes supported by <a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a> are supported by this API.  If the <i>FileAttributes</i> and <i>ReparseTag</i> can’t be extracted from a given information class, this API will return CF_PLACEHOLDER_STATE_INVALID and set last error properly.