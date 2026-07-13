---
UID: NF:textserv.IRicheditUiaOverrides.GetPropertyOverrideValue
title: IRicheditUiaOverrides::GetPropertyOverrideValue (textserv.h)
description: Retrieves the host container's override value for the specified Microsoft UI Automation accessibility property of a windowless rich edit control.
helpviewer_keywords: ["GetPropertyOverrideValue","GetPropertyOverrideValue method [Windows Controls]","GetPropertyOverrideValue method [Windows Controls]","IRicheditUiaOverrides interface","IRicheditUiaOverrides interface [Windows Controls]","GetPropertyOverrideValue method","IRicheditUiaOverrides.GetPropertyOverrideValue","IRicheditUiaOverrides::GetPropertyOverrideValue","controls.irichedituiaoverrides_getpropertyoverridevalue","textserv/IRicheditUiaOverrides::GetPropertyOverrideValue"]
old-location: controls\irichedituiaoverrides_getpropertyoverridevalue.htm
tech.root: Controls
ms.assetid: C949A3DA-F98E-4035-8986-A76EB8F54558
ms.date: 12/05/2018
ms.keywords: GetPropertyOverrideValue, GetPropertyOverrideValue method [Windows Controls], GetPropertyOverrideValue method [Windows Controls],IRicheditUiaOverrides interface, IRicheditUiaOverrides interface [Windows Controls],GetPropertyOverrideValue method, IRicheditUiaOverrides.GetPropertyOverrideValue, IRicheditUiaOverrides::GetPropertyOverrideValue, controls.irichedituiaoverrides_getpropertyoverridevalue, textserv/IRicheditUiaOverrides::GetPropertyOverrideValue
req.header: textserv.h
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRicheditUiaOverrides::GetPropertyOverrideValue
 - textserv/IRicheditUiaOverrides::GetPropertyOverrideValue
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
 - IRicheditUiaOverrides.GetPropertyOverrideValue
---

# IRicheditUiaOverrides::GetPropertyOverrideValue


## -description

Retrieves the host container's override value for the specified Microsoft UI Automation accessibility property of a windowless rich edit control.

## -parameters

### -param propertyId

Type: <b>PROPERTYID </b>

The identifier of the property to retrieve.

### -param pRetValue

Type: <b>VARIANT*</b>

The host container's override value for the <i>propertyId</i> property.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/textserv/nn-textserv-irichedituiaoverrides">IRicheditUiaOverrides</a>