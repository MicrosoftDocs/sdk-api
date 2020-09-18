---
UID: NF:setupapi.SetupDiGetClassImageList
title: SetupDiGetClassImageList function (setupapi.h)
description: The SetupDiGetClassImageList function builds an image list that contains bitmaps for every installed class and returns the list in a data structure.
helpviewer_keywords: ["SetupDiGetClassImageList","SetupDiGetClassImageList function [Device and Driver Installation]","devinst.setupdigetclassimagelist","di-rtns_ef2c4660-f78a-4228-9b24-9c84e38765e5.xml","setupapi/SetupDiGetClassImageList"]
old-location: devinst\setupdigetclassimagelist.htm
tech.root: devinst
ms.assetid: d6b84403-9284-4fba-a419-a013cf68ea1e
ms.date: 12/05/2018
ms.keywords: SetupDiGetClassImageList, SetupDiGetClassImageList function [Device and Driver Installation], devinst.setupdigetclassimagelist, di-rtns_ef2c4660-f78a-4228-9b24-9c84e38765e5.xml, setupapi/SetupDiGetClassImageList
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
 - SetupDiGetClassImageList
 - setupapi/SetupDiGetClassImageList
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
 - SetupDiGetClassImageList
---

# SetupDiGetClassImageList function


## -description

The <b>SetupDiGetClassImageList</b> function builds an image list that contains bitmaps for every installed class and returns the list in a data structure.

## -parameters

### -param ClassImageListData [out]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_classimagelist_data">SP_CLASSIMAGELIST_DATA</a> structure to receive information regarding the class image list, including a handle to the image list. The <b>cbSize</b> field of this structure must be initialized with the size of the structure, in bytes, before calling this function or it will fail.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The image list built by this function should be destroyed by calling <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidestroyclassimagelist">SetupDiDestroyClassImageList</a>.

Call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassimagelistexa">SetupDiGetClassImageListEx</a> to retrieve the image list for classes installed on a remote computer.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidestroyclassimagelist">SetupDiDestroyClassImageList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassimagelistexa">SetupDiGetClassImageListEx</a>