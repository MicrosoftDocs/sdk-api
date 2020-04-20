---
UID: NF:cfapi.CfGetPlaceholderRangeInfo
title: CfGetPlaceholderRangeInfo function (cfapi.h)
description: Gets range information about a placeholder file or folder.helpviewer_keywords: ["CfGetPlaceholderRangeInfo","CfGetPlaceholderRangeInfo function","cfapi/CfGetPlaceholderRangeInfo","cloudApi.cfgetplaceholderrangeinfo"]
old-location: cloudapi\cfgetplaceholderrangeinfo.htm
tech.root: cfApi
ms.assetid: B7FE94BC-DC59-407D-85A6-9657E38975AB
ms.date: 12/05/2018
ms.keywords: CfGetPlaceholderRangeInfo, CfGetPlaceholderRangeInfo function, cfapi/CfGetPlaceholderRangeInfo, cloudApi.cfgetplaceholderrangeinfo
f1_keywords:
- cfapi/CfGetPlaceholderRangeInfo
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- CldApi.dll
api_name:
- CfGetPlaceholderRangeInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CfGetPlaceholderRangeInfo function


## -description


Gets range information about a placeholder file or folder.


## -parameters




### -param FileHandle [in]

The handle of the placeholder file to be queried.


### -param InfoClass [in]

Types of the range of placeholder data.


### -param StartingOffset [in]

Offset of the starting point of the range of data.


### -param Length [in]

Length of the range of data.


### -param InfoBuffer [out]

Pointer to a buffer to receive the data.


### -param InfoBufferLength [in]

Length, in bytes, of <i>InfoBuffer</i>.


### -param ReturnedLength [out, optional]

The length of the returned range of placeholder data in the <i>InfoBuffer</i>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Unlike most placeholder APIs that take a file handle, this one does not modify the file in any way, therefore the file handle only requires READ_ATTRIBUTES access.



