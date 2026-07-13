---
UID: NF:useractivityinterop.IUserActivitySourceHostInterop.SetActivitySourceHost
tech.root: winrt
title: IUserActivitySourceHostInterop::SetActivitySourceHost
ms.date: 04/16/2021
targetos: Windows
description: Associates host information with either a [UserActivityChannel](/uwp/api/windows.applicationmodel.useractivities.useractivitychannel) or the [UserActivity](/uwp/api/windows.applicationmodel.useractivities.useractivity) object.
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
 - IUserActivitySourceHostInterop::SetActivitySourceHost
f1_keywords:
 - IUserActivitySourceHostInterop::SetActivitySourceHost
 - useractivityinterop/IUserActivitySourceHostInterop::SetActivitySourceHost
dev_langs:
 - c++
---

## -description

Associates host information with either a [UserActivityChannel](/uwp/api/windows.applicationmodel.useractivities.useractivitychannel) or the [UserActivity](/uwp/api/windows.applicationmodel.useractivities.useractivity) object.

## -parameters

### -param activitySourceHost

An **HSTRING** containing the host to be associated with the user activity.

## -returns

If this function succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.


## -remarks

The host information for a **UserActivity** object only needs to set with this method if the **UserActivity** object was constructed from a source other than a **UserActivityChannel**, such as by using the **UserActivity** constructor. 

## -see-also

