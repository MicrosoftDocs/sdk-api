---
UID: NF:setupapi.SetupDiDestroyClassImageList
title: SetupDiDestroyClassImageList function (setupapi.h)
description: The SetupDiDestroyClassImageList function destroys a class image list that was built by a call to SetupDiGetClassImageList or SetupDiGetClassImageListEx.
helpviewer_keywords: ["SetupDiDestroyClassImageList","SetupDiDestroyClassImageList function [Device and Driver Installation]","devinst.setupdidestroyclassimagelist","di-rtns_15428f4d-4785-460b-9da1-746cf2c69159.xml","setupapi/SetupDiDestroyClassImageList"]
old-location: devinst\setupdidestroyclassimagelist.htm
tech.root: devinst
ms.assetid: 47ccc16c-b061-489b-b534-5b5929c5d010
ms.date: 12/05/2018
ms.keywords: SetupDiDestroyClassImageList, SetupDiDestroyClassImageList function [Device and Driver Installation], devinst.setupdidestroyclassimagelist, di-rtns_15428f4d-4785-460b-9da1-746cf2c69159.xml, setupapi/SetupDiDestroyClassImageList
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
 - SetupDiDestroyClassImageList
 - setupapi/SetupDiDestroyClassImageList
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
 - SetupDiDestroyClassImageList
---

# SetupDiDestroyClassImageList function


## -description

The <b>SetupDiDestroyClassImageList</b> function destroys a class image list that was built by a call to <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassimagelist">SetupDiGetClassImageList</a> or <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassimagelistexa">SetupDiGetClassImageListEx</a>.

## -parameters

### -param ClassImageListData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_classimagelist_data">SP_CLASSIMAGELIST_DATA</a> structure that contains the class image list to destroy.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassimagelist">SetupDiGetClassImageList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassimagelistexa">SetupDiGetClassImageListEx</a>