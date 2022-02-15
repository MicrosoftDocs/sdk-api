---
UID: NF:commoncontrols.ImageList_CoCreateInstance
title: ImageList_CoCreateInstance function (commoncontrols.h)
description: Creates a single instance of an imagelist and returns an interface pointer to it.
helpviewer_keywords: ["ImageList_CoCreateInstance","ImageList_CoCreateInstance function [Windows Controls]","_shell_ImageList_CoCreateInstance","_shell_ImageList_CoCreateInstance_cpp","commoncontrols/ImageList_CoCreateInstance","controls.ImageList_CoCreateInstance","controls._shell_ImageList_CoCreateInstance"]
old-location: controls\ImageList_CoCreateInstance.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_cocreateinstance.htm
ms.date: 12/05/2018
ms.keywords: ImageList_CoCreateInstance, ImageList_CoCreateInstance function [Windows Controls], _shell_ImageList_CoCreateInstance, _shell_ImageList_CoCreateInstance_cpp, commoncontrols/ImageList_CoCreateInstance, controls.ImageList_CoCreateInstance, controls._shell_ImageList_CoCreateInstance
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImageList_CoCreateInstance
 - commoncontrols/ImageList_CoCreateInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - ImageList_CoCreateInstance
---

# ImageList_CoCreateInstance function


## -description

Creates a single instance of an imagelist and returns an interface pointer to it.

## -parameters

### -param rclsid [in]

Type: <b>REFCLSID</b>

A reference to the CLSID—a GUID that identifies the COM object to be created. This should be <b>CLSID_ImageList</b>.

### -param punkOuter [in, optional]

Type: <b>const <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the outer <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface that aggregates the object created by this function, or <b>NULL</b> if no aggregation is desired.

### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired interface ID.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is normally <a href="/windows/desktop/api/commoncontrols/nn-commoncontrols-iimagelist2">IImageList2</a>, which provides the <a href="/windows/desktop/api/commoncontrols/nf-commoncontrols-iimagelist2-initialize">Initialize</a> method.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Before calling this function, COM must be initialized by calling <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>.

Call <b>ImageList_CoCreateInstance</b> for a customized image list; otherwise, call <a href="/windows/desktop/api/shellapi/nf-shellapi-shgetimagelist">SHGetImageList</a> to load the system image list. Call <a href="/windows/desktop/api/shellapi/nf-shellapi-shgetfileinfoa">SHGetFileInfo</a> with the <i>uflag</i> parameter set to <b>SHGFI_SYSICONINDEX</b> to retrieve a handle to the system image list.