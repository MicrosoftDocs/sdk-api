---
UID: NF:setupapi.SetupDiGetClassImageListExA
title: SetupDiGetClassImageListExA function (setupapi.h)
description: The SetupDiGetClassImageListEx function builds an image list of bitmaps for every class installed on a local or remote system. (ANSI)
helpviewer_keywords: ["SetupDiGetClassImageListExA", "di-rtns_ff251460-9ebf-4968-80f2-f44c13305197.xml"]
old-location: devinst\setupdigetclassimagelistex.htm
tech.root: devinst
ms.assetid: f9cf7904-3fda-4f7f-bb05-3634fd1c9af3
ms.date: 01/30/2023
ms.keywords: SetupDiGetClassImageListEx, SetupDiGetClassImageListEx function [Device and Driver Installation], SetupDiGetClassImageListExA, SetupDiGetClassImageListExW, devinst.setupdigetclassimagelistex, di-rtns_ff251460-9ebf-4968-80f2-f44c13305197.xml, setupapi/SetupDiGetClassImageListEx
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiGetClassImageListExA
 - setupapi/SetupDiGetClassImageListExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiGetClassImageListEx - SetupDiGetClassImageListExA
---

# SetupDiGetClassImageListExA function


## -description

The <b>SetupDiGetClassImageListEx</b> function builds an image list of bitmaps for every class installed on a local or remote system.

## -parameters

### -param ClassImageListData [out]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_classimagelist_data">SP_CLASSIMAGELIST_DATA</a> structure to receive information regarding the class image list, including a handle to the image list. The <b>cbSize</b> field of this structure must be initialized with the size of the structure, in bytes, before calling this function or it will fail.

### -param MachineName [in, optional]

A pointer to NULL-terminated string that supplies the name of a remote system for whose classes <b>SetupDiGetClassImageListEx must build</b> the bitmap. This parameter is optional and can be <b>NULL</b>. If <i>MachineName</i> is <b>NULL</b>, <b>SetupDiGetClassImageListEx</b> builds the list for the local system.

> [!CAUTION]
> Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.

### -param Reserved

Must be <b>NULL</b>.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The image list built by this function should be destroyed by calling <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidestroyclassimagelist">SetupDiDestroyClassImageList</a>.

<div class="alert"><b>Note</b>    Class-specific icons on a remote computer can only be displayed if the class is also present on the local computer. Thus, if the remote computer has class <i>X</i>, but class <i>X</i> is not installed locally, then the generic (unknown) icon will be returned.</div>
<div> </div>




> [!NOTE]
> The setupapi.h header defines SetupDiGetClassImageListEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidestroyclassimagelist">SetupDiDestroyClassImageList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassimagelist">SetupDiGetClassImageList</a>
