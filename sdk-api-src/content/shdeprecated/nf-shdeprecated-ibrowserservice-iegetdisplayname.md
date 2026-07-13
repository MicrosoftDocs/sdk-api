---
UID: NF:shdeprecated.IBrowserService.IEGetDisplayName
title: IBrowserService::IEGetDisplayName (shdeprecated.h)
description: Deprecated. Retrieves the URL that corresponds to a pointer to an item identifier list (PIDL).
helpviewer_keywords: ["IBrowserService interface [Windows Shell]","IEGetDisplayName method","IBrowserService.IEGetDisplayName","IBrowserService::IEGetDisplayName","IEGetDisplayName","IEGetDisplayName method [Windows Shell]","IEGetDisplayName method [Windows Shell]","IBrowserService interface","SHGDN_FORADDRESSBAR","SHGDN_FORPARSING","SHGDN_NORMAL","shdeprecated/IBrowserService::IEGetDisplayName","shell.IBrowserService_IEGetDisplayName","zone_IBrowserService_IEGetDisplayName"]
old-location: shell\IBrowserService_IEGetDisplayName.htm
tech.root: shell
ms.assetid: 012d794a-9823-4af2-b628-ad33a93dbbb5
ms.date: 12/05/2018
ms.keywords: IBrowserService interface [Windows Shell],IEGetDisplayName method, IBrowserService.IEGetDisplayName, IBrowserService::IEGetDisplayName, IEGetDisplayName, IEGetDisplayName method [Windows Shell], IEGetDisplayName method [Windows Shell],IBrowserService interface, SHGDN_FORADDRESSBAR, SHGDN_FORPARSING, SHGDN_NORMAL, shdeprecated/IBrowserService::IEGetDisplayName, shell.IBrowserService_IEGetDisplayName, zone_IBrowserService_IEGetDisplayName
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
 - IBrowserService::IEGetDisplayName
 - shdeprecated/IBrowserService::IEGetDisplayName
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
 - IBrowserService.IEGetDisplayName
---

# IBrowserService::IEGetDisplayName


## -description

Deprecated. Retrieves the URL that corresponds to a pointer to an item identifier list (PIDL).

## -parameters

### -param pidl [in]

Type: <b>LPCITEMIDLIST</b>

The PIDL for which to get the corresponding URL.

### -param pwszName [out]

Type: <b>LPWSTR</b>

A pointer to a buffer of at least INTERNET_MAX_URL_LENGTH characters to receive the URL.

### -param uFlags [in]

Type: <b>UINT</b>

One of the following values specifying the form of the retrieved URL.



#### SHGDN_NORMAL (0)

The URL is relative to the folder from which the request was made. SHGDN_NORMAL is equivalent to <b>NULL</b> and therefore should not be combined with other flags.



#### SHGDN_FORADDRESSBAR (0)

The URL is suitable for display in an address bar combo box.



#### SHGDN_FORPARSING (0)

The URL can be used for parsing.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

