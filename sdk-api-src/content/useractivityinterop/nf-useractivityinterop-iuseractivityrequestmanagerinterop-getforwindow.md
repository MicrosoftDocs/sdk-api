---
UID: NF:useractivityinterop.IUserActivityRequestManagerInterop.GetForWindow
tech.root: winrt
title: IUserActivityRequestManagerInterop::GetForWindow
ms.date: 04/16/2021
targetos: Windows
description: Creates a [UserActivityRequestManager](/uwp/api/windows.applicationmodel.useractivities.useractivityrequestmanager) associated with the specified window.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: useractivityinterop.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - useractivityinterop.h
api_name:
 - IUserActivityRequestManagerInterop::GetForWindow
f1_keywords:
 - IUserActivityRequestManagerInterop::GetForWindow
 - useractivityinterop/IUserActivityRequestManagerInterop::GetForWindow
dev_langs:
 - c++
---

## -description

Creates a [UserActivityRequestManager](/uwp/api/windows.applicationmodel.useractivities.useractivityrequestmanager) associated with the specified window.

## -parameters

### -param window

Handle to the window of the active application.

### -param iid

The GUID for the resource interface.

The REFIID, or GUID, of the interface to the resource can be obtained by using the __uuidof() macro. For example: 

`__uuidof(UserActivityRequestManager)` 

### -param value

Address of a pointer to a [UserActivityRequestManager](/uwp/api/windows.applicationmodel.useractivities.useractivityrequestmanager) object.

## -returns

If this function succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.


## -remarks

## -see-also

