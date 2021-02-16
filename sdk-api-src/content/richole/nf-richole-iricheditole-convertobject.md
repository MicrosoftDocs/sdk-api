---
UID: NF:richole.IRichEditOle.ConvertObject
title: IRichEditOle::ConvertObject (richole.h)
description: Converts an object to a new type. This call reloads the object but does not force an update; the caller must do this.
helpviewer_keywords: ["ConvertObject","ConvertObject method [Windows Controls]","ConvertObject method [Windows Controls]","IRichEditOle interface","IRichEditOle interface [Windows Controls]","ConvertObject method","IRichEditOle.ConvertObject","IRichEditOle::ConvertObject","_win32_IRichEditOle_ConvertObject","_win32_IRichEditOle_ConvertObject_cpp","controls.IRichEditOle_ConvertObject","controls._win32_IRichEditOle_ConvertObject","richole/IRichEditOle::ConvertObject"]
old-location: controls\IRichEditOle_ConvertObject.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditoleconvertobject.htm
ms.date: 12/05/2018
ms.keywords: ConvertObject, ConvertObject method [Windows Controls], ConvertObject method [Windows Controls],IRichEditOle interface, IRichEditOle interface [Windows Controls],ConvertObject method, IRichEditOle.ConvertObject, IRichEditOle::ConvertObject, _win32_IRichEditOle_ConvertObject, _win32_IRichEditOle_ConvertObject_cpp, controls.IRichEditOle_ConvertObject, controls._win32_IRichEditOle_ConvertObject, richole/IRichEditOle::ConvertObject
req.header: richole.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRichEditOle::ConvertObject
 - richole/IRichEditOle::ConvertObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRichEditOle.ConvertObject
---

# IRichEditOle::ConvertObject


## -description

Converts an object to a new type. This call reloads the object but does not force an update; the caller must do this.

## -parameters

### -param iob

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Index of the object to convert. If this parameter is REO_IOB_SELECTION, the selected object is to be converted.

### -param rclsidNew

Type: <b>REFCLSID</b>

Class identifier of the class to which the object is converted.

### -param lpstrUserTypeNew

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

User-visible type name of the class to which the object is converted.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise. E_INVALIDARG is returned if the index is invalid.

## -see-also

<a href="/windows/desktop/api/richole/nn-richole-iricheditole">IRichEditOle</a>