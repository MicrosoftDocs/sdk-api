---
UID: NF:shlobj_core.ILLoadFromStreamEx
title: ILLoadFromStreamEx function (shlobj_core.h)
description: This function may be altered or unavailable.helpviewer_keywords: ["ILLoadFromStreamEx","ILLoadFromStreamEx function [Windows Shell]","ILLoadFromStreamEx(IStream*","PIDLIST_ABSOLUTE*)","_shell_ILLoadFromStreamEx_IStream_PIDLIST_ABSOLUTE","shell.ILLoadFromStreamEx_IStream_PIDLIST_ABSOLUTE","shlobj_core/ILLoadFromStreamEx"]
old-location: shell\ILLoadFromStreamEx_IStream_PIDLIST_ABSOLUTE.htm
tech.root: shell
ms.assetid: 6fb735b6-a8c3-439e-9f20-4fda8f008b28
ms.date: 12/05/2018
ms.keywords: ILLoadFromStreamEx, ILLoadFromStreamEx function [Windows Shell], ILLoadFromStreamEx(IStream*,PIDLIST_ABSOLUTE*), _shell_ILLoadFromStreamEx_IStream_PIDLIST_ABSOLUTE, shell.ILLoadFromStreamEx_IStream_PIDLIST_ABSOLUTE, shlobj_core/ILLoadFromStreamEx
f1_keywords:
- shlobj_core/ILLoadFromStreamEx
dev_langs:
- c++
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- shlobj_core.h
- Windows.Storage.dll
api_name:
- ILLoadFromStreamEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILLoadFromStreamEx function


## -description


<p class="CCE_Message">[<b>ILLoadFromStreamEx(IStream*, PIDLIST_ABSOLUTE*)</b> 
    is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Loads an absolute <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> from an 
    <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>.


## -parameters




### -param pstm [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface from which the absolute 
      <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> loads.


### -param pidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

When this method returns and succeeds, contains the resulting absolute 
      <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>. If it fails, contains 
      <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For use where STRICT_TYPED_ITEMIDS is defined.



