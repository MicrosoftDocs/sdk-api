---
UID: NF:setupapi.SetupDiGetClassBitmapIndex
title: SetupDiGetClassBitmapIndex function (setupapi.h)
description: The SetupDiGetClassBitmapIndex function retrieves the index of the mini-icon supplied for the specified class.
helpviewer_keywords: ["SetupDiGetClassBitmapIndex","SetupDiGetClassBitmapIndex function [Device and Driver Installation]","devinst.setupdigetclassbitmapindex","di-rtns_6c4b7a43-90cf-4f8a-9766-2ebe966fb8c0.xml","setupapi/SetupDiGetClassBitmapIndex"]
old-location: devinst\setupdigetclassbitmapindex.htm
tech.root: devinst
ms.assetid: 5e64d387-701c-42eb-87a8-ba2f51c8552d
ms.date: 12/05/2018
ms.keywords: SetupDiGetClassBitmapIndex, SetupDiGetClassBitmapIndex function [Device and Driver Installation], devinst.setupdigetclassbitmapindex, di-rtns_6c4b7a43-90cf-4f8a-9766-2ebe966fb8c0.xml, setupapi/SetupDiGetClassBitmapIndex
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiGetClassBitmapIndex
 - setupapi/SetupDiGetClassBitmapIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupDiGetClassBitmapIndex
---

# SetupDiGetClassBitmapIndex function


## -description

The <b>SetupDiGetClassBitmapIndex</b> function retrieves the index of the mini-icon supplied for the specified class.

## -parameters

### -param ClassGuid [in, optional]

A pointer to the GUID of the <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a> for which to retrieve the mini-icon. This pointer is optional and can be <b>NULL</b>.

### -param MiniIconIndex [out]

A pointer to a variable of type INT that receives the index of the mini-icon for the specified device setup class. If the <i>ClassGuid</i> parameter is <b>NULL</b> or if there is no mini-icon for the specified class, <b>SetupDiGetClassBitmapIndex</b> returns the index of the mini-icon for the Unknown device setup class.

## -returns

If there is a min-icon for the specified device setup class, <b>SetupDiGetClassBitmapIndex</b> returns <b>TRUE</b>. Otherwise, this function returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the <i>ClassGuid</i> parameter is <b>NULL</b>, or if there is no mini-icon for the specified class, the function returns <b>FALSE</b> and <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_NO_DEVICE_ICON.

## -remarks

For a list of the device setup class mini-icons and their corresponding indexes, see <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidrawminiicon">SetupDiDrawMiniIcon</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidrawminiicon">SetupDiDrawMiniIcon</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiloadclassicon">SetupDiLoadClassIcon</a>