---
UID: NF:strmif.IAMPluginControl.SetDisabled
title: IAMPluginControl::SetDisabled (strmif.h)
description: Adds a class identifier (CLSID) to the blocked list, or removes a CLSID from the list.
helpviewer_keywords: ["IAMPluginControl interface [DirectShow]","SetDisabled method","IAMPluginControl.SetDisabled","IAMPluginControl::SetDisabled","SetDisabled","SetDisabled method [DirectShow]","SetDisabled method [DirectShow]","IAMPluginControl interface","dshow.iamplugincontrol_setdisabled","strmif/IAMPluginControl::SetDisabled"]
old-location: dshow\iamplugincontrol_setdisabled.htm
tech.root: dshow
ms.assetid: 3ac4b3b5-0882-4e30-b3fa-1dcee33a74d3
ms.date: 12/05/2018
ms.keywords: IAMPluginControl interface [DirectShow],SetDisabled method, IAMPluginControl.SetDisabled, IAMPluginControl::SetDisabled, SetDisabled, SetDisabled method [DirectShow], SetDisabled method [DirectShow],IAMPluginControl interface, dshow.iamplugincontrol_setdisabled, strmif/IAMPluginControl::SetDisabled
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMPluginControl::SetDisabled
 - strmif/IAMPluginControl::SetDisabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMPluginControl.SetDisabled
---

# IAMPluginControl::SetDisabled


## -description

Adds a class identifier (CLSID) to the blocked list, or removes a CLSID from the list.

## -parameters

### -param clsid [in]

The CLSID to add or remove.

### -param disabled [in]

Specifies whether to add or remove the CSLID. If the value is <b>TRUE</b>, the method adds the CLSID to the blocked list. Otherwise, the method removes it from the list.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-iamplugincontrol">IAMPluginControl</a>



<a href="/windows/desktop/DirectShow/intelligent-connect">Intelligent Connect</a>