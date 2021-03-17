---
UID: NF:setupapi.SetupDiGetHwProfileList
title: SetupDiGetHwProfileList function (setupapi.h)
description: The SetupDiGetHwProfileList function retrieves a list of all currently defined hardware profile IDs.
helpviewer_keywords: ["SetupDiGetHwProfileList","SetupDiGetHwProfileList function [Device and Driver Installation]","devinst.setupdigethwprofilelist","di-rtns_fb906b00-dab3-4cb0-88a9-b54f719211c9.xml","setupapi/SetupDiGetHwProfileList"]
old-location: devinst\setupdigethwprofilelist.htm
tech.root: devinst
ms.assetid: 59fc7202-0e03-4eaa-b3ca-7d55be767b1a
ms.date: 12/05/2018
ms.keywords: SetupDiGetHwProfileList, SetupDiGetHwProfileList function [Device and Driver Installation], devinst.setupdigethwprofilelist, di-rtns_fb906b00-dab3-4cb0-88a9-b54f719211c9.xml, setupapi/SetupDiGetHwProfileList
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
 - SetupDiGetHwProfileList
 - setupapi/SetupDiGetHwProfileList
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
 - SetupDiGetHwProfileList
---

# SetupDiGetHwProfileList function


## -description

The <b>SetupDiGetHwProfileList</b> function retrieves a list of all currently defined hardware profile IDs.

## -parameters

### -param HwProfileList [out]

A pointer to an array to receive the list of currently defined hardware profile IDs.

### -param HwProfileListSize [in]

The number of DWORDs in the <i>HwProfileList</i> buffer.

### -param RequiredSize [out]

A pointer to a variable of type DWORD that receives the number of hardware profiles currently defined. If the number is larger than <i>HwProfileListSize</i>, the list is truncated to fit the array size. The value returned in <i>RequiredSize</i> indicates the array size required to store the entire list of hardware profiles. In this case, the function fails and a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER.

### -param CurrentlyActiveIndex [out, optional]

A pointer to a variable of type DWORD that receives the index of the currently active hardware profile in the retrieved hardware profile list. This parameter is optional and can be <b>NULL</b>.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigethwprofilelistexa">SetupDiGetHwProfileListEx</a> to retrieve the hardware profile IDs for a remote computer.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedevregkeya">SetupDiCreateDevRegKey</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopendevregkey">SetupDiOpenDevRegKey</a>