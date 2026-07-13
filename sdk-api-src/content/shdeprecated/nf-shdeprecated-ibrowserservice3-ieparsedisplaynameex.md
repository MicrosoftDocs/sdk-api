---
UID: NF:shdeprecated.IBrowserService3.IEParseDisplayNameEx
title: IBrowserService3::IEParseDisplayNameEx (shdeprecated.h)
description: Deprecated. Parses a URL into a pointer to an item identifier list (PIDL). (IBrowserService3.IEParseDisplayNameEx)
helpviewer_keywords: ["IBrowserService3 interface [Windows Shell]","IEParseDisplayNameEx method","IBrowserService3.IEParseDisplayNameEx","IBrowserService3::IEParseDisplayNameEx","IEPDN_BINDINGUI","IEParseDisplayNameEx","IEParseDisplayNameEx method [Windows Shell]","IEParseDisplayNameEx method [Windows Shell]","IBrowserService3 interface","shdeprecated/IBrowserService3::IEParseDisplayNameEx","shell.IBrowserService3_IEParseDisplayNameEx","zone_IBrowserService3_IEParseDisplayNameEx"]
old-location: shell\IBrowserService3_IEParseDisplayNameEx.htm
tech.root: shell
ms.assetid: 9e36418e-026b-4682-9074-4caec5370f8b
ms.date: 12/05/2018
ms.keywords: IBrowserService3 interface [Windows Shell],IEParseDisplayNameEx method, IBrowserService3.IEParseDisplayNameEx, IBrowserService3::IEParseDisplayNameEx, IEPDN_BINDINGUI, IEParseDisplayNameEx, IEParseDisplayNameEx method [Windows Shell], IEParseDisplayNameEx method [Windows Shell],IBrowserService3 interface, shdeprecated/IBrowserService3::IEParseDisplayNameEx, shell.IBrowserService3_IEParseDisplayNameEx, zone_IBrowserService3_IEParseDisplayNameEx
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.product: Internet Explorer 6.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService3::IEParseDisplayNameEx
 - shdeprecated/IBrowserService3::IEParseDisplayNameEx
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
 - IBrowserService3.IEParseDisplayNameEx
---

# IBrowserService3::IEParseDisplayNameEx


## -description

Deprecated. Parses a URL into a pointer to an item identifier list (PIDL).

## -parameters

### -param uiCP

Type: <b>UINT</b>

The code page (for example, CP_ACP, the system default code page).

### -param pwszPath

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the URL to parse, as a Unicode string.

### -param dwFlags

Type: <b>DWORD</b>

The following value, if desired.



#### IEPDN_BINDINGUI (0x00000001)

Display a UI element during binding.

### -param ppidlOut

Type: <b>LPITEMIDLIST*</b>

The PIDL created from the parsed URL.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method replaces <a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-ieparsedisplayname">IEParseDisplayName</a>.
