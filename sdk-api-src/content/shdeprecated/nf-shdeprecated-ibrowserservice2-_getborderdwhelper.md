---
UID: NF:shdeprecated.IBrowserService2._GetBorderDWHelper
title: IBrowserService2::_GetBorderDWHelper (shdeprecated.h)
description: Deprecated. A helper method for the implementation of GetBorderDW.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_GetBorderDWHelper method","IBrowserService2._GetBorderDWHelper","IBrowserService2::_GetBorderDWHelper","_GetBorderDWHelper","_GetBorderDWHelper method [Windows Shell]","_GetBorderDWHelper method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_GetBorderDWHelper","shell.IBrowserService2__GetBorderDWHelper","zone_IBrowserService2__GetBorderDWHelper"]
old-location: shell\IBrowserService2__GetBorderDWHelper.htm
tech.root: shell
ms.assetid: 44477311-61c6-48d0-bef8-349ca114a891
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_GetBorderDWHelper method, IBrowserService2._GetBorderDWHelper, IBrowserService2::_GetBorderDWHelper, _GetBorderDWHelper, _GetBorderDWHelper method [Windows Shell], _GetBorderDWHelper method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_GetBorderDWHelper, shell.IBrowserService2__GetBorderDWHelper, zone_IBrowserService2__GetBorderDWHelper
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.product: Internet Explorer 5.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService2::_GetBorderDWHelper
 - shdeprecated/IBrowserService2::_GetBorderDWHelper
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
 - IBrowserService2._GetBorderDWHelper
---

# IBrowserService2::_GetBorderDWHelper


## -description

Deprecated. A helper method for the implementation of <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-idockingwindowsite-getborderdw">GetBorderDW</a>.

## -parameters

### -param punkSrc [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> that represents the object for which the border space is being requested.

### -param lprectBorder [in]

Type: <b>LPRECT</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the dimensions of the available border space for the browser.

### -param bUseHmonitor [in]

Type: <b>BOOL</b>

A value of type <b>BOOL</b> that indicates whether to use an <b>HMONITOR</b> to determine the display. <b>TRUE</b> to use the <b>HMONITOR</b>; <b>FALSE</b> to ignore the particular display in the size determination.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.