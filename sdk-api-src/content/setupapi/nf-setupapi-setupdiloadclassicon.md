---
UID: NF:setupapi.SetupDiLoadClassIcon
title: SetupDiLoadClassIcon function (setupapi.h)
description: The SetupDiLoadClassIcon function loads both the large and mini-icon for the specified class.
helpviewer_keywords: ["SetupDiLoadClassIcon","SetupDiLoadClassIcon function [Device and Driver Installation]","devinst.setupdiloadclassicon","di-rtns_968c659d-6f45-4416-beb9-8fa25c4c060e.xml","setupapi/SetupDiLoadClassIcon"]
old-location: devinst\setupdiloadclassicon.htm
tech.root: devinst
ms.assetid: f239e207-fb51-4641-a64c-7d8ffa767e18
ms.date: 12/05/2018
ms.keywords: SetupDiLoadClassIcon, SetupDiLoadClassIcon function [Device and Driver Installation], devinst.setupdiloadclassicon, di-rtns_968c659d-6f45-4416-beb9-8fa25c4c060e.xml, setupapi/SetupDiLoadClassIcon
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
 - SetupDiLoadClassIcon
 - setupapi/SetupDiLoadClassIcon
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
 - SetupDiLoadClassIcon
---

# SetupDiLoadClassIcon function


## -description

The <b>SetupDiLoadClassIcon</b> function loads both the large and mini-icon for the specified class.

## -parameters

### -param ClassGuid [in]

A pointer to the GUID of the class for which the icon(s) should be loaded.

### -param LargeIcon [out, optional]

A pointer to an icon handle that receives the handle value for the loaded large icon for the specified class. This pointer is optional and can be <b>NULL</b>. If the pointer is <b>NULL</b>, the large icon is not loaded.

### -param MiniIconIndex [out, optional]

A pointer to an INT-typed variable that receives the index of the mini-icon for the specified class. The mini-icon is stored in the device installer's mini-icon cache. The pointer is optional and can be <b>NULL</b>.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The icons of the class are either predefined and loaded from the device installer's internal cache, or they are loaded directly from the class installer's executable. This function queries the registry value <b>ICON</b> in the specified class's section. If the <b>ICON</b> value is specified, it indicates which mini-icon to load. 

If the <b>ICON</b> value is negative, the absolute value represents a predefined icon in the class's registry. See <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidrawminiicon">SetupDiDrawMiniIcon</a> for a list of the predefined mini-icons. 

If the <b>ICON</b> value is positive, it represents an icon in the class installer's executable image that will be extracted. The value 1 is reserved. This function also uses the <b>INSTALLER32</b> registry value and then the <b>ENUMPROPPAGES32</b> registry value to determine which executable image to extract the icons from. For more information about these registry values, see <a href="/windows-hardware/drivers/install/inf-classinstall32-section">INF ClassInstall32 Section</a>.

When a caller is finished using the icon, the caller must call <b>DestroyIcon</b> (which is described in the Microsoft Windows SDK documentation).

If the <i>LargeIcon </i> parameter is specified, but the <i>ClassGuid</i> parameter does not supply a valid class GUID or the <b>Icon</b> registry value of the class is not valid, <b>SetupDiLoadClassIcon</b> loads the default large icon, returns the handle for the large icon, and, if the <i>MiniIconIndex</i> parameter is specified, returns the index of the default mini-icon.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidrawminiicon">SetupDiDrawMiniIcon</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassbitmapindex">SetupDiGetClassBitmapIndex</a>