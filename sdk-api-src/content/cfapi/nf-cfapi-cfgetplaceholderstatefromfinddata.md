---
UID: NF:cfapi.CfGetPlaceholderStateFromFindData
title: CfGetPlaceholderStateFromFindData function (cfapi.h)
description: Gets a set of placeholder states based on the WIN32_FIND_DATA structure.
helpviewer_keywords: ["CfGetPlaceholderStateFromFindData","CfGetPlaceholderStateFromFindData function","cfapi/CfGetPlaceholderStateFromFindData","cloudApi.cfgetplaceholderstatefromfinddata"]
old-location: cloudapi\cfgetplaceholderstatefromfinddata.htm
tech.root: cloudapi
ms.assetid: 1A8104BC-E9D1-4846-B91F-4CBEDB1FC542
ms.date: 03/30/2023
ms.keywords: CfGetPlaceholderStateFromFindData, CfGetPlaceholderStateFromFindData function, cfapi/CfGetPlaceholderStateFromFindData, cloudApi.cfgetplaceholderstatefromfinddata
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
 - CfGetPlaceholderStateFromFindData
 - cfapi/CfGetPlaceholderStateFromFindData
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
 - CfGetPlaceholderStateFromFindData
---

# CfGetPlaceholderStateFromFindData function

## -description

Gets a set of placeholder states based on the [WIN32_FIND_DATA](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) structure.

## -parameters

### -param FindData [in]

The find data information on the file.

## -returns

Can include [CF_PLACEHOLDER_STATE](ne-cfapi-cf_placeholder_state.md); the placeholder state.

## -remarks

The **WIN32_FIND_DATA** structure is obtained from the [FindFirstFile](/windows/win32/api/fileapi/nf-fileapi-findfirstfilea)/[FindNextFile](/windows/win32/api/fileapi/nf-fileapi-findnextfilea) functions.

## -see-also

[WIN32_FIND_DATA](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa)

[CF_PLACEHOLDER_STATE](ne-cfapi-cf_placeholder_state.md)

[FindFirstFile](/windows/win32/api/fileapi/nf-fileapi-findfirstfilea)

[FindNextFile](/windows/win32/api/fileapi/nf-fileapi-findnextfilea)
