---
UID: NF:shdeprecated.IBrowserService.IEParseDisplayName
title: IBrowserService::IEParseDisplayName (shdeprecated.h)
description: Deprecated. Parses a URL into a pointer to an item identifier list (PIDL). (IBrowserService.IEParseDisplayName)
helpviewer_keywords: ["IBrowserService interface [Windows Shell]","IEParseDisplayName method","IBrowserService.IEParseDisplayName","IBrowserService::IEParseDisplayName","IEParseDisplayName","IEParseDisplayName method [Windows Shell]","IEParseDisplayName method [Windows Shell]","IBrowserService interface","shdeprecated/IBrowserService::IEParseDisplayName","shell.IBrowserService_IEParseDisplayName","zone_IBrowserService_IEParseDisplayName"]
old-location: shell\IBrowserService_IEParseDisplayName.htm
tech.root: shell
ms.assetid: 02f5a6cb-2f90-4613-80cd-1e8a47bb32c2
ms.date: 12/05/2018
ms.keywords: IBrowserService interface [Windows Shell],IEParseDisplayName method, IBrowserService.IEParseDisplayName, IBrowserService::IEParseDisplayName, IEParseDisplayName, IEParseDisplayName method [Windows Shell], IEParseDisplayName method [Windows Shell],IBrowserService interface, shdeprecated/IBrowserService::IEParseDisplayName, shell.IBrowserService_IEParseDisplayName, zone_IBrowserService_IEParseDisplayName
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService::IEParseDisplayName
 - shdeprecated/IBrowserService::IEParseDisplayName
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
 - IBrowserService.IEParseDisplayName
---

# IBrowserService::IEParseDisplayName


## -description

Deprecated. Parses a URL into a pointer to an item identifier list (PIDL).

## -parameters

### -param uiCP [in]

Type: <b>UINT</b>

A value of type <b>UINT</b> that indicates the code page (for example, CP_ACP, the system default code page) to use in the parsing.

### -param pwszPath [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the URL as a Unicode string.

### -param ppidlOut [out]

Type: <b>LPITEMIDLIST*</b>

The PIDL created from the parsed URL.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

