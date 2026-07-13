---
UID: NF:wia_xp.IWiaItemExtras.GetExtendedErrorInfo
title: IWiaItemExtras::GetExtendedErrorInfo (wia_xp.h)
description: The IWiaItemExtras::GetExtendedErrorInfo method gets a string from the device driver that contains information about the most recent error.
helpviewer_keywords: ["GetExtendedErrorInfo","GetExtendedErrorInfo method [WIA]","GetExtendedErrorInfo method [WIA]","IWiaItemExtras interface","IWiaItemExtras interface [WIA]","GetExtendedErrorInfo method","IWiaItemExtras.GetExtendedErrorInfo","IWiaItemExtras::GetExtendedErrorInfo","_wia_IWiaItemExtras_GetExtendedErrorInfo","wia._wia_IWiaItemExtras_GetExtendedErrorInfo","wia_xp/IWiaItemExtras::GetExtendedErrorInfo"]
old-location: wia\_wia_IWiaItemExtras_GetExtendedErrorInfo.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitemextras\getextendederrorinfo.htm
ms.date: 12/05/2018
ms.keywords: GetExtendedErrorInfo, GetExtendedErrorInfo method [WIA], GetExtendedErrorInfo method [WIA],IWiaItemExtras interface, IWiaItemExtras interface [WIA],GetExtendedErrorInfo method, IWiaItemExtras.GetExtendedErrorInfo, IWiaItemExtras::GetExtendedErrorInfo, _wia_IWiaItemExtras_GetExtendedErrorInfo, wia._wia_IWiaItemExtras_GetExtendedErrorInfo, wia_xp/IWiaItemExtras::GetExtendedErrorInfo
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWiaItemExtras::GetExtendedErrorInfo
 - wia_xp/IWiaItemExtras::GetExtendedErrorInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaItemExtras.GetExtendedErrorInfo
archived: true
---

# IWiaItemExtras::GetExtendedErrorInfo


## -description

The <b>IWiaItemExtras::GetExtendedErrorInfo</b> method gets a string from the device driver that contains information about the most recent error. Call this method after an error during an operation on a Windows Image Acquisition (WIA) item (such as data transfer).

## -parameters

### -param bstrErrorText [out]

Type: <b>BSTR*</b>

Pointer to a string that contains the error information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Applications must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to free the string to which <i>bstrErrorText</i> points.

## -see-also

<a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitemextras">IWiaItemExtras</a>