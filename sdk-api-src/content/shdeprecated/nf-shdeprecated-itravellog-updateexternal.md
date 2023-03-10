---
UID: NF:shdeprecated.ITravelLog.UpdateExternal
title: ITravelLog::UpdateExternal (shdeprecated.h)
description: Deprecated. Updates an entry that originated out of the current procedure through IHlinkFrame.
helpviewer_keywords: ["ITravelLog interface [Windows Shell]","UpdateExternal method","ITravelLog.UpdateExternal","ITravelLog::UpdateExternal","UpdateExternal","UpdateExternal method [Windows Shell]","UpdateExternal method [Windows Shell]","ITravelLog interface","shdeprecated/ITravelLog::UpdateExternal","shell.ITravelLog_UpdateExternal","zone_ITravelLog_UpdateExternal"]
old-location: shell\ITravelLog_UpdateExternal.htm
tech.root: shell
ms.assetid: 2fda446d-8652-455b-9233-aa02f2a85e7f
ms.date: 12/05/2018
ms.keywords: ITravelLog interface [Windows Shell],UpdateExternal method, ITravelLog.UpdateExternal, ITravelLog::UpdateExternal, UpdateExternal, UpdateExternal method [Windows Shell], UpdateExternal method [Windows Shell],ITravelLog interface, shdeprecated/ITravelLog::UpdateExternal, shell.ITravelLog_UpdateExternal, zone_ITravelLog_UpdateExternal
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
 - ITravelLog::UpdateExternal
 - shdeprecated/ITravelLog::UpdateExternal
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
 - ITravelLog.UpdateExternal
---

# ITravelLog::UpdateExternal


## -description

Deprecated. Updates an entry that originated out of the current procedure through <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)">IHlinkFrame</a>.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> representing the nearest browser or frame within which the travel generating the log is taking place.

### -param punkHLBrowseContext [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of an <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)">IHlinkBrowseContext</a> retrieved through <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767937(v=vs.85)">IHlinkFrame::GetBrowseContext</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.