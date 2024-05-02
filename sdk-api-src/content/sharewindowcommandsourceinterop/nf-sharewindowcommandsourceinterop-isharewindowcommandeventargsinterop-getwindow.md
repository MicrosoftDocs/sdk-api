---
UID: NF:sharewindowcommandsourceinterop.IShareWindowCommandEventArgsInterop.GetWindow
title: IShareWindowCommandEventArgsInterop::GetWindow
description: Gets the window identifier (a window handle).
prerelease: false
ms.date: 06/09/2021
tech.root: winrt
req.header: sharewindowcommandsourceinterop.h
req.include-header: 
req.construct-type: function
req.target-type: Windows
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
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
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sharewindowcommandsourceinterop.h
api_name:
 - IShareWindowCommandEventArgsInterop::GetWindow
f1_keywords:
 - IShareWindowCommandEventArgsInterop::GetWindow
 - sharewindowcommandsourceinterop/IShareWindowCommandEventArgsInterop::GetWindow
---

## -description

Gets the window identifier (a window handle).

> [!IMPORTANT]
> The **IShareWindowCommandEventArgsInterop::GetWindow** API is part of a Limited Access Feature (see [LimitedAccessFeatures class](/uwp/api/windows.applicationmodel.limitedaccessfeatures)). For more information or to request an unlock token, contact [Microsoft Support](https://aka.ms/LAFAccessRequests).

## -parameters

### -param value

Type: **[HWND](/windows/win32/winprog/windows-data-types)\***

The address of a **HWND** in which to receive the window identifier (a window handle).

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

For a code example, see [IShareWindowCommandEventArgsInterop](nn-sharewindowcommandsourceinterop-isharewindowcommandeventargsinterop.md).

## -see-also

* [IShareWindowCommandEventArgsInterop](nn-sharewindowcommandsourceinterop-isharewindowcommandeventargsinterop.md)
