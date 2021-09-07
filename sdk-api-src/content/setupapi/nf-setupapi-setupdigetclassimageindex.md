---
UID: NF:setupapi.SetupDiGetClassImageIndex
title: SetupDiGetClassImageIndex function (setupapi.h)
description: The SetupDiGetClassImageIndex function retrieves the index within the class image list of a specified class.
helpviewer_keywords: ["SetupDiGetClassImageIndex","SetupDiGetClassImageIndex function [Device and Driver Installation]","devinst.setupdigetclassimageindex","di-rtns_6f022ba0-12d8-47f4-9e7f-27f94dbe9b71.xml","setupapi/SetupDiGetClassImageIndex"]
old-location: devinst\setupdigetclassimageindex.htm
tech.root: devinst
ms.assetid: 56c17b9a-d516-4903-90fc-efac22e1f50d
ms.date: 12/05/2018
ms.keywords: SetupDiGetClassImageIndex, SetupDiGetClassImageIndex function [Device and Driver Installation], devinst.setupdigetclassimageindex, di-rtns_6f022ba0-12d8-47f4-9e7f-27f94dbe9b71.xml, setupapi/SetupDiGetClassImageIndex
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
 - SetupDiGetClassImageIndex
 - setupapi/SetupDiGetClassImageIndex
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
 - SetupDiGetClassImageIndex
---

# SetupDiGetClassImageIndex function


## -description

The <b>SetupDiGetClassImageIndex</b> function retrieves the index within the class image list of a specified class.

## -parameters

### -param ClassImageListData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_classimagelist_data">SP_CLASSIMAGELIST_DATA</a> structure that describes a class image list that includes the image for the <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a> that is specified by the <i>ClassGuid</i> parameter.

### -param ClassGuid [in]

A pointer to the GUID of the device setup class for which to retrieve the index of the class image in the specified class image list.

### -param ImageIndex [out]

A pointer to an INT-typed variable that receives the index of the specified class image in the class image list.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the specified device setup class is not included in the specified class image list, <b>SetupDiGetClassImageIndex</b> returns the image index for the Unknown device setup class in the <i>ImageIndex</i> parameter.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassimagelist">SetupDiGetClassImageList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassimagelistexa">SetupDiGetClassImageListEx</a>